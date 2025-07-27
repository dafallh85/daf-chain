# daf chain (DAF1)

🚀 A decentralized token on the BNB Smart Chain (BEP-20), designed to power a new era of digital payments, smart utilities, and Web3 integration.

---

## 📄 Token Details

- **Token Name:** daf chain
- **Symbol:** DAF1
- **Decimals:** 18
- **Total Supply:** 100,000,000,000,000 (100 Trillion)
- **Contract Address:** [`0x0C9a6b4Bd24d69812B8f3A71a56DA686C9110012`](https://bscscan.com/token/0x0C9a6b4Bd24d69812B8f3A71a56DA686C9110012)
- **Blockchain:** BNB Chain (BEP-20)

---

## 🌐 Official Links

- 🌍 Website: [https://dafchain.com](https://dafchain.com)
- ✉️ Email: daf1@dafchain.com
- 🐦 Twitter: [@daf1chain](https://x.com/daf1chain)
- 📢 Telegram Channel: [DAFChoin](https://t.me/DAFChoin)
- 📬 Telegram Contact: [DAF_Choin](https://t.me/DAF_Choin)
- 💬 Community Discussions: [DAF1Choin Group](https://t.me/DAF1Choin)
// [Add contract code or link to Token.sol here]
https://bscscan.com/token/0x0C9a6b4Bd24d69812B8f3A71a56DA686C9110012
he ---
---

## ⚙️ Smart Contract

Tpragma solidity ^0.8.2;
/**
 *Submitted for verification at BscScan.com on 2025-03-09
*/

pragma solidity ^0.8.2;

contract Token {
    mapping(address => uint) public balances;
    mapping(address => mapping(address => uint)) public allowance;
    uint public totalSupply = 100000000000000 * 10 ** 18;
    string public name = "daf chain";
    string public symbol = "DAF1";
    uint public decimals = 18;
    
    event Transfer(address indexed from, address indexed to, uint value);
    event Approval(address indexed owner, address indexed spender, uint value);
    
    constructor() {
        balances[msg.sender] = totalSupply;
    }
    
    function balanceOf(address owner) public returns(uint) {
        return balances[owner];
    }
    
    function transfer(address to, uint value) public returns(bool) {
        require(balanceOf(msg.sender) >= value, 'balance too low');
        balances[to] += value;
        balances[msg.sender] -= value;
       emit Transfer(msg.sender, to, value);
        return true;
    }
    
    function transferFrom(address from, address to, uint value) public returns(bool) {
        require(balanceOf(from) >= value, 'balance too low');
        require(allowance[from][msg.sender] >= value, 'allowance too low');
        balances[to] += value;
        balances[from] -= value;
        emit Transfer(from, to, value);
        return true;   
    }
    
    function approve(address spender, uint value) public returns (bool) {
        allowance[msg.sender][spender] = value;
        emit Approval(msg.sender, spender, value);
        return true;   
    }
}
## 📂 Repository Structure

sdaf-chain
│
├── Token.sol             # Smart Contract Source Code
├── README.md             # Project Description and Info
├── LICENSE               # MIT License
└── logo.png              # Token Logo (Already Added)mart contract is written in Solidity and follows BEP-20 standards.
---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
