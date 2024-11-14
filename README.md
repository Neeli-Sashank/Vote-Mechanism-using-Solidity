VotingWithPause Smart Contract

VotingWithPause is a Solidity-based smart contract for a simple, Ether-based voting system with built-in emergency pause functionality. It enables secure voting on the blockchain, with the owner able to add candidates, manage voting, and control funds collected.
Features

    Candidate Management: Only the contract owner can add candidates to the election.
    Ether-Based Voting: Each vote is cast by sending a small amount of Ether to the contract, ensuring each vote is traceable to a transaction.
    Voting Limitations: Voters can only vote once, and each vote is tied to the candidate specified.
    Pause and Resume Functionality: The contract includes an emergency stop feature, allowing the owner to pause or resume voting as needed.
    Funds Management: Only the owner can withdraw the Ether collected from votes.

Key Functions

    addCandidate(string memory _name): Adds a new candidate (only owner).
    vote(uint _candidateId): Casts a vote for a candidate by sending Ether.
    pause(): Pauses voting (only owner).
    resume(): Resumes voting after a pause (only owner).
    getCandidateVoteCount(uint _candidateId): Returns the current vote count for a specific candidate.
    withdrawFunds(): Allows the owner to withdraw collected funds.

Events

    CandidateAdded(uint candidateId, string name): Logs when a candidate is added.
    Voted(address voter, uint candidateId): Logs when a user votes.
    Paused(): Logs when the contract is paused.
    Resumed(): Logs when the contract is resumed.

Usage Notes

    Owner Role: The deployer of the contract becomes the owner and has exclusive rights to pause, resume, add candidates, and withdraw funds.
    One Vote per Address: Each address can vote only once to maintain fairness.
