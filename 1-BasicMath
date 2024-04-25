// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract BasicMath {
  uint256 constant MAX_INT = type(uint256).max;

  function adder(uint256 _a, uint256 _b) external pure returns (uint256 sum, bool error) {
    if (_b > MAX_INT - _a) {
      return (0, true); // Overflow occurred
    }
    return (_a + _b, false);
  }

  function subtractor(uint256 _a, uint256 _b) external pure returns (uint256 difference, bool error) {
    if (_b > _a) {
      return (0, true); // Underflow occurred
    }
    return (_a - _b, false);
  }

  function multiplier(uint256 _a, uint256 _b) external pure returns (uint256 product, bool error) {
    // Check for overflow during multiplication
    if (_a == 0 || _b > MAX_INT / _a) {
      return (0, true); // Overflow occurred
    }
    return (_a * _b, false);
  }

  function modulo(uint256 _a, uint256 _b) external pure returns (uint256 remainder, bool error) {
    // Solidity requires the divisor to be greater than zero for modulo operation
    require(_b > 0, "Divisor cannot be zero");
    return (_a % _b, false);
  }
}
