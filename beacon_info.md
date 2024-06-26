# Beacon Information

Prior to the start of the ceremony, we declared on-chain the selection of a specific Ethereum block number, which yields a remainder of 92,194 when divided by 200,000. The hash of this block is used as input to generate our random beacon with 2^34 BLAKE2b iterations for the zkTrue-up circuit.

*   The Ethereum Transaction Hash For Storing The Declaration: [0x1ac72f51dec26094b9c752d4ae02c375df87b67d09ac1ba00d6d41d632282ece](https://etherscan.io/tx/0x1ac72f51dec26094b9c752d4ae02c375df87b67d09ac1ba00d6d41d632282ece)
*   The Ethereum block number of this transaction: [19859915](https://etherscan.io/block/19859915)
*   Declaration (utf-8 encoded):

    ```
    In the trusted setup ceremony for the zkTrue-up circuit, we plan to apply a random beacon generated through the computation of a Verifiable Delay Function (VDF) on a specific block hash from the Ethereum mainnet. We will select the block number that, when divided by 200,000, results in a remainder of 92,194, and use the hash of this block as the input for our computations. The designated random beacon will be the outcome of 2^34 iterations of the BLAKE2b hash of this block's hash value.

    Given the Proof of Stake (PoS) mechanism in Ethereum, when two consecutive blocks are endorsed by the majority of validators and deemed "justified," the first block is subsequently "finalized." The maximum duration from a block being chained to it being finalized is roughly 12.8 minutes (spanning two Epochs). Hence, as long as it is confirmed that the block proposer cannot compute the 2^34 BLAKE2b hash iterations within 12.8 minutes, the security of this random beacon can be trusted.

    The BLAKE2b hash of evacu_0000.zkey is: 7e3ed951fee7523a628bc61c487173831fa4a89fc83f1e0532574cc7f6b18f9cfe26ad070f28e26f34a24c289d4a9359ca85a40e84df6d5e16cf99aebf1e0ba1

    The BLAKE2b hash of normal_0000.zkey is: 042170b92756e63f2a0b2e32eee9ed0cbff37d71de187a7bb1c961b370c284f53e8969f6b2fe07c04d5f3cc6c50adb5f444af244d13ca24753b769ec2d6359c2
    ```

The finalized zkey files:

*   [normal_finalized.zkey](https://storage.googleapis.com/trusted-setup.v1.zktrue-up.ts.finance/normal_finalized.zkey)
*   [evacu_finalized.zkey](https://storage.googleapis.com/trusted-setup.v1.zktrue-up.ts.finance/evacu_finalized.zkey)

The random beacon is the 2 ^ 34 iteration of BLAKE2b over the hash of [the 19892194th Ethereum block](https://etherscan.io/block/19892194). The hash is:

```
0x0dc48c8c525657e9e45b156937c50566c0462552c6e728a79d73d48f75f69e57
```

Clearly, the 19892194th Ethereum block appeared significantly later than the 19859915th block.

Below is a list of every 2^29 iterations computed by the beacon:

```
Iteration 00536870912: Hash = 0x712a83a17adbb5ae5294a63518d956d66cffa8108c0a927b7dc88a827d8bb05482f7bf82d8555ad7744403f2a4cd1144980d4efbe7c02bd682b7cef2b167a53d
Iteration 01073741824: Hash = 0x04cd8df9e8020b5d08a3e329c84f8c3346e5cea7cc1d88ecb677d5058f790ca3e71d98c8854dd18c7f730e9f3d41bf7c926f880c0f32e62c87e3cd9dbaa0ff4c
Iteration 01610612736: Hash = 0x56acef3730453e615ada29c2ccd31a5ea12777631a1ec50bbe7be4cb8cb249433c44de0558dcca1311cfe9f30bdebbd858eff7afdd8863f1dbc4d1b8a01e8abf
Iteration 02147483648: Hash = 0x31ce0750fbb297b28853ff7fec281f6cf5e6f18d72be63b6886293970daf345c6b4cb171cc7c5a610e9bbdbdf685d2451e57aed0062130e87ece76e54c550feb
Iteration 02684354560: Hash = 0xbb7f97034139a88dce44ef1cd531914939b8fdfc432a23eafe6fb0fc543bc5f7db5e813eee35be7a0988eeaac2a56243c09c717e3c4e5e05a9bfdae72a83251b
Iteration 03221225472: Hash = 0x19e30343e699e377327d77bbb5766ddffaba8ea89e6ea72db816e6246372ab87fc75da03afd0a8500dfe214bb73885679a1d90e67bd6a455a1e94c08a2a6c6f1
Iteration 03758096384: Hash = 0xe953902534fc8536c12abf0aafd4a7806cd25463495743239c62a19ea3b419ee1aacee8e04b06088b6a43c7a4f12cfbc44ea9eb387e87b00e19facdfdad74a5e
Iteration 04294967296: Hash = 0x024b1fcb4f81218c4c0d29075a8ca034959b91cca59c3d2bbf8169a2834c793eaef74d44c87cba002370880510e2f8605fd82831eb5a1056a3d5e2d7d1f9735a
Iteration 04831838208: Hash = 0x801cdf5fe68e9dd8d661b22e7d04dacd124f1bb0ffa1a175d36ddc643a03d57b64df369bbfdb1954dd81e54311a513ebfb0d9ddffbc16b257775a6284a5d3cc7
Iteration 05368709120: Hash = 0x04dda1307951fe4ba90f45772f7752f34b5bbc056758bea8c794ec8f27f6695783e5f6dea14311219c44912515793b799057a56d0404e7060a55a254f8a6b426
Iteration 05905580032: Hash = 0x562db5416db6c54aee4b0f6652f4eee080cce57d3f8772eda2badf6fd341647ca710e066bde84ef900f1d2e51e95d95ef8fde84a454d5573e20247d3057be9cc
Iteration 06442450944: Hash = 0x3337a73164ce29738c3c3312652274e45358013bfcd6ed18ac89b6fc32e66e8967db6daec97ef733042f847897387cf20356f3abe9c8e32ab0954d78ccaa7160
Iteration 06979321856: Hash = 0x461a59ef46ab7591900731405c1c920a99819ea78e8b802d5f41007911307fbf71692aeee3829b8170ee4c068ee365c03435c2d40f845385e2fa4af1e31986e0
Iteration 07516192768: Hash = 0x728e700ea4346bc4649e90a442fdecdef86aab5a64d0d34ed50f59caad80f70f077c43aba4ab0cf7bf1ad03b76398b2815078b7eae7ae0b8edde579904d078d6
Iteration 08053063680: Hash = 0x76a0f93ae3715a2227a552df4593f9cbd7b92ac90b7482fdca8fb1f2a05f4fd90aa2f4f136cc86fc38c7c841f22028c28ae7e7d8a502184b6e23c72a68ad8f25
Iteration 08589934592: Hash = 0xe02f9bbc11df58ce79b7bbe9c7af647295cbc8ce7a560c32bb4f3a99d70490c3fbe17cfdfae7175d3cc12d93a7fe70a56ec4415d264bfd1b350cba2c7f1cb251
Iteration 09126805504: Hash = 0x1fd10e52b928a370882660e02406d7c26e689a0f35a8126801aa5f60273aebf919b9a99c54e0a3d55f5579cecbe670c631c3a62c29da98c3c271e9f3c500c92f
Iteration 09663676416: Hash = 0xf1a186ac72690511fcc40f824d778aa9050754827b3e41a95216e50d126a93e3006deae37f45691af19b09d403975b1f1ab9eaf9762cc7b585b6b6ba7db8b5a7
Iteration 10200547328: Hash = 0xe7e7c2665b8b0f6e907e36da21b80d067bfa3b69fe706adae932807f1c046d4abe5c609aba801bdc3168d4801210f976d0dcee3dfe08ba9f01dcdb5bc477cca1
Iteration 10737418240: Hash = 0x23a5e3bf323241e6fc080b1197b1ce2821f5a781568de86c765e9f18ec1cac2985dfa887d551dbc3edd7fc3f1d7d00a41b2be8490bee8ea957ab7c2338cb26b8
Iteration 11274289152: Hash = 0x5b657a04e4312abe3c62ca7065f1a50852e278907853df36e42cd0d1ae7a55715cc0aa70e32fc82d634ec8c67f9da4c489d989de44724b9b590185293b7a82b4
Iteration 11811160064: Hash = 0x1771ae2478ea430a681dcf1aa9a1eb9787f4fc33e0a07837185505b592f78a78ad818dabd5bba6433c6d44cb25fab553b71c4fd196c564524993fec147b4c270
Iteration 12348030976: Hash = 0xce1b9b036d86c26f762c571d8a75b07b9a6e4ad01b6909e4b5bcecc23f174af15a65be07a223b6cc827f328b2e5f6c29279ae4c48f5ed2f196a73b2fb9bd9570
Iteration 12884901888: Hash = 0x9ae5a2a0ca8009b374cec18d7e021d3b46415cc464a5a555d196cab9b5e17703ad2d6b1f2545aa296db5fd2899e2afcd94b56364b89744bdb32395a955c6177e
Iteration 13421772800: Hash = 0x5ccf5229b364cf1ba6d065a1aa0c29ee8c0b2802bd1c17dc8d299a42e2860a357a74588139b6aa98bd93655394042987e54fc4c4360d819c6108da4bb62a5fa6
Iteration 13958643712: Hash = 0xa856a7209bc2336a6c1793c34908d246e6cb04f6e973315127ddd5bff8fdc934e2d4277fe640d1ae02880e8bb4d0037e5dca99db9fcb9ab4283dd8efe3f2dbef
Iteration 14495514624: Hash = 0x38c76245ee47f95aa8dd9c24d26ff33e38da2a2d4ccc7c0b40d595a3f24cfc5463fd251202617ab0538913c90f212999d808766e8757d5b7aa473b8ca22ed6f1
Iteration 15032385536: Hash = 0x662aefce24ab8faff70cb8b57716d0da74663c2f22b6e5ad0ad9753a0cde95809eab43ad6f1109c87e31a46cc8d8c814460fb9a5fa7c517354beab22570d90b3
Iteration 15569256448: Hash = 0xeb19ca2426dde7f6cf55022a5018bd90bec9b9f22ea17a0acff7e7fc12c6efad8c7a966463cf588069674f9d44c409d8cca7b8670c971d4350c4f0ca5f42acd9
Iteration 16106127360: Hash = 0x21c35ff5c0db4e7ec5fb21e122e81000735f9d9920a7b1c791c88d12e42942371e0a9312916a663f201c30edf39b151b12815344e63764c0501d3f5f8dfabe22
Iteration 16642998272: Hash = 0x4b32bd57957a3cc7cb18760ed2b891b18041302ccdc53645521c320e07391c7434ec2683e5046ca4453d01ea0d7ecf914021a59ea2334fc6407c827c449bc49f
Iteration 17179869184: Hash = 0xc2927a3ec362c356e59b0b59e1a565088ff1af7370f11cfc4c240cd47181b8f554e5bdf38198fd577f6f8a32a5c777ca65578408582d1d356f81f26a6d10b024
```