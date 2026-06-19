python -m tests.run_all                                                                           
                            
============================================================
[ RUNNING ] tests.test_vm
============================================================
STACK PUSH: 02aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
OP_DUP
OP_HASH160

STACK:
0: 02aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
1: 64096dffec1b1b52addf3020a9f01be8b812c3f9

[ PASS ] tests.test_vm

============================================================
[ RUNNING ] tests.test_script
============================================================
>>> PUSH 02aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
>>> OP_DUP
>>> OP_HASH160

[ SCRIPT SUCCESS ]

STACK:
0: 02aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
1: 64096dffec1b1b52addf3020a9f01be8b812c3f9

[ PASS ] tests.test_script

============================================================
[ RUNNING ] tests.test_p2pkh
============================================================
PUBKEY: 0464322d8cb79ddbcd659875434b827d84828fe172b3e042dda1ea93f4a016853c7f4fa61d8c725d1d7286851485af15daff44aefd215798b2f74e2a1bbf0de030
PUBKEY HASH: 8c882f31f68ed09516665977f6870b0be1325b70
SIGNATURE: 304502201cce13f6626d155e13c6e1ebf3646ba6889d6a4155c073da6c9c01aeada1e8f402210099c39e05068380dfc04e68d482a2b55a7e94fa7440c9203cdb015a5a418c8624
>>> PUSH 304502201cce13f6626d155e13c6e1ebf3646ba6889d6a4155c073da6c9c01aeada1e8f402210099c39e05068380dfc04e68d482a2b55a7e94fa7440c9203cdb015a5a418c8624
>>> PUSH 0464322d8cb79ddbcd659875434b827d84828fe172b3e042dda1ea93f4a016853c7f4fa61d8c725d1d7286851485af15daff44aefd215798b2f74e2a1bbf0de030
>>> OP_DUP
>>> OP_HASH160
>>> PUSH 8c882f31f68ed09516665977f6870b0be1325b70
>>> OP_EQUALVERIFY
[ EQUALVERIFY SUCCESS ]
>>> OP_CHECKSIG
[ CHECKSIG ERROR ] Missing message hash
[ SCRIPT FAILED ]

[ PASS ] tests.test_p2pkh

============================================================
[ RUNNING ] tests.test_schnorr
============================================================

SCHNORR SUMMARY:
{'valid_length': True, 'has_sighash': False, 'byte_length': 64}

[ PASS ] tests.test_schnorr

============================================================
[ RUNNING ] tests.test_taproot_detect
============================================================

KEY PATH:
{'witness_items': 1, 'key_path': True, 'script_path': False, 'annex_present': False, 'control_block_present': False, 'tap_script_present': False, 'schnorr_signature_present': True, 'schnorr_signature': {'valid_length': True, 'has_sighash': False, 'byte_length': 64}}

SCHNORR SIG:
aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

SCRIPT PATH:
{'witness_items': 3, 'key_path': False, 'script_path': False, 'annex_present': False, 'control_block_present': True, 'tap_script_present': True, 'schnorr_signature_present': True, 'schnorr_signature': {'valid_length': True, 'has_sighash': False, 'byte_length': 64}}

[ PASS ] tests.test_taproot_detect

============================================================
[ RUNNING ] tests.test_schnorr_vector
============================================================

BIP340 VECTOR RESULT:
True

[ PASS ] tests.test_schnorr_vector

============================================================
[ RUNNING ] tests.test_validator
============================================================
>>> PUSH 304502200ad55043dd935703c413c2afbec8c60524793975a0a68c6d624747ac398707c2022100cb84abdeac5b35147795b1bc7a7f1177b51aa02306a409a8bfc854e01d69577301
>>> PUSH 0485bc010d94a2117b9a426463fb5781301e9069c8991071508006b585f98fe78437c6c0b9c036ebc5a78122e7d2ed688248eb914e0c0a23697c3e1f9e56f0f0d8
>>> OP_DUP
>>> OP_HASH160
>>> PUSH cf42ce3584dc48b10817c432543bfab8bce1bbf2
>>> OP_EQUALVERIFY
[ EQUALVERIFY SUCCESS ]
>>> OP_CHECKSIG

[ SCRIPT SUCCESS ]

STACK:
0: True
{'type': 'P2PKH', 'valid': True, 'script_result': 'PASS', 'engine': 'Arkeon Core Validator', 'trace': [{'op': 'PUSH', 'value': '304502200ad55043dd935703c413c2afbec8c60524793975a0a68c6d624747ac398707c2022100cb84abdeac5b35147795b1bc7a7f1177b51aa02306a409a8bfc854e01d69577301', 'stack_depth': 1}, {'op': 'PUSH', 'value': '0485bc010d94a2117b9a426463fb5781301e9069c8991071508006b585f98fe78437c6c0b9c036ebc5a78122e7d2ed688248eb914e0c0a23697c3e1f9e56f0f0d8', 'stack_depth': 2}, {'op': 'OP_DUP', 'result': 'PASS', 'stack_depth': 3}, {'op': 'OP_HASH160', 'result': 'PASS', 'hash': 'cf42ce3584dc48b10817c432543bfab8bce1bbf2', 'stack_depth': 3}, {'op': 'PUSH', 'value': 'cf42ce3584dc48b10817c432543bfab8bce1bbf2', 'stack_depth': 4}, {'op': 'OP_EQUALVERIFY', 'result': 'PASS', 'stack_depth': 2}, {'op': 'OP_CHECKSIG', 'result': 'PASS', 'stack_depth': 1}]}

[ PASS ] tests.test_validator

============================================================
[ RUNNING ] tests.test_p2tr_preview
============================================================
P2TR PREVIEW ERROR: Unexpected EOF

[ PASS ] tests.test_p2tr_preview

============================================================
[ RUNNING ] tests.test_core_vectors
============================================================

[ PASS ] tests.test_core_vectors

============================================================
[ RUNNING ] tests.test_tapscript_minimalif_valid
============================================================
[OK] MINIMALIF valid passed

[ PASS ] tests.test_tapscript_minimalif_valid

============================================================
[ RUNNING ] tests.test_tapscript_minimalif_invalid
============================================================
[OK] MINIMALIF invalid rejected

[ PASS ] tests.test_tapscript_minimalif_invalid

============================================================
[ RUNNING ] tests.test_tapscript_if_else
============================================================
[OK] OP_IF false branch + OP_ELSE passed

[ PASS ] tests.test_tapscript_if_else

============================================================
[ RUNNING ] tests.test_tapscript_unclosed_if
============================================================
[OK] unclosed IF rejected

[ PASS ] tests.test_tapscript_unclosed_if

============================================================
[ RUNNING ] tests.test_tapscript_op_success
============================================================
[OK] OP_SUCCESSx passed

[ PASS ] tests.test_tapscript_op_success

============================================================
[ RUNNING ] tests.test_tapscript_codeseparator
============================================================
[OK] OP_CODESEPARATOR tracking passed

[ PASS ] tests.test_tapscript_codeseparator

============================================================
[ RUNNING ] tests.test_tapscript_stack_limit
============================================================
[OK] stack limit rejected

[ PASS ] tests.test_tapscript_stack_limit

============================================================
[ RUNNING ] tests.test_tapscript_stack_item_size
============================================================
[OK] stack item size rejected

[ PASS ] tests.test_tapscript_stack_item_size

============================================================
[ RUNNING ] tests.test_tapscript_equalverify
============================================================
[OK] OP_EQUALVERIFY passed

[ PASS ] tests.test_tapscript_equalverify

============================================================
[ RUNNING ] tests.test_tapscript_script_size
============================================================
[OK] script size limit rejected

[ PASS ] tests.test_tapscript_script_size

============================================================
[ RUNNING ] tests.test_real_flow
============================================================
Z: 44f04c00bc1e481cf53c54f9311f41de37a499967abff116133d0fa103ced437
>>> PUSH 304402200a569c0875d5feff8c0975471fa994de831cc05acbcb5baadcf8b02eff6c1f1c02206d704527b549dbd56decd1913d8dee689600e3fcc75c985507bbb95608aa8ead01
>>> PUSH 04100de52edb63eefb2c7bd45e7a9706c85de8c549fd8b20fda5bd4bb0a35451648192a04c7addba49ab3c57c6b768573a15b9142c27d3e168fa1f3098c86d7039
>>> OP_DUP
>>> OP_HASH160
>>> PUSH 40f98f4fe93837ea54987e1f45f195ac328f3a4c
>>> OP_EQUALVERIFY
[ EQUALVERIFY SUCCESS ]
>>> OP_CHECKSIG

[ SCRIPT SUCCESS ]

STACK:
0: True
{'type': 'P2PKH', 'valid': True, 'script_result': 'PASS', 'engine': 'Arkeon Core Validator', 'trace': [{'op': 'PUSH', 'value': '304402200a569c0875d5feff8c0975471fa994de831cc05acbcb5baadcf8b02eff6c1f1c02206d704527b549dbd56decd1913d8dee689600e3fcc75c985507bbb95608aa8ead01', 'stack_depth': 1}, {'op': 'PUSH', 'value': '04100de52edb63eefb2c7bd45e7a9706c85de8c549fd8b20fda5bd4bb0a35451648192a04c7addba49ab3c57c6b768573a15b9142c27d3e168fa1f3098c86d7039', 'stack_depth': 2}, {'op': 'OP_DUP', 'result': 'PASS', 'stack_depth': 3}, {'op': 'OP_HASH160', 'result': 'PASS', 'hash': '40f98f4fe93837ea54987e1f45f195ac328f3a4c', 'stack_depth': 3}, {'op': 'PUSH', 'value': '40f98f4fe93837ea54987e1f45f195ac328f3a4c', 'stack_depth': 4}, {'op': 'OP_EQUALVERIFY', 'result': 'PASS', 'stack_depth': 2}, {'op': 'OP_CHECKSIG', 'result': 'PASS', 'stack_depth': 1}]}

[ PASS ] tests.test_real_flow

============================================================
[ RUNNING ] tests.test_pipeline_full
============================================================

RAW TX:
02000000010000000000000000000000000000000000000000000000000000000000000000000000008c493046022100de507bc43dd2ac72eeb291e75008063d4d80d0969e35e3cd5d8b11b4c1b647a3022100904929baeaccdec2088ba0bdb5e92611bde40a8ca87c0d71e4accc10b425a7f80141048d89ef7a3f2f02f7bd54b47c2f8b641abc807b20c79e2d58b921a04e94778dd4130c062f9f9a86ff10008eca6917f2a1cee3cf62e7d7b7e742d5018a66365b9dffffffff0198ecfa02000000001976a9144f1f14899c66c1b7d41c1bfec2158ea969ddf8d188ac00000000

BUILDER Z:
e4c51f8c2c505d8b6fc40d27a7a557723a531bb590b7157b30d349c104e9230e
>>> PUSH 3046022100de507bc43dd2ac72eeb291e75008063d4d80d0969e35e3cd5d8b11b4c1b647a3022100904929baeaccdec2088ba0bdb5e92611bde40a8ca87c0d71e4accc10b425a7f801
>>> PUSH 048d89ef7a3f2f02f7bd54b47c2f8b641abc807b20c79e2d58b921a04e94778dd4130c062f9f9a86ff10008eca6917f2a1cee3cf62e7d7b7e742d5018a66365b9d
>>> OP_DUP
>>> OP_HASH160
>>> PUSH 4f1f14899c66c1b7d41c1bfec2158ea969ddf8d1
>>> OP_EQUALVERIFY
[ EQUALVERIFY SUCCESS ]
>>> OP_CHECKSIG

[ SCRIPT SUCCESS ]

STACK:
0: True

PIPELINE RESULT:
{'type': 'P2PKH', 'valid': True, 'script_result': 'PASS', 'engine': 'Arkeon Core Validator', 'trace': [{'op': 'PUSH', 'value': '3046022100de507bc43dd2ac72eeb291e75008063d4d80d0969e35e3cd5d8b11b4c1b647a3022100904929baeaccdec2088ba0bdb5e92611bde40a8ca87c0d71e4accc10b425a7f801', 'stack_depth': 1}, {'op': 'PUSH', 'value': '048d89ef7a3f2f02f7bd54b47c2f8b641abc807b20c79e2d58b921a04e94778dd4130c062f9f9a86ff10008eca6917f2a1cee3cf62e7d7b7e742d5018a66365b9d', 'stack_depth': 2}, {'op': 'OP_DUP', 'result': 'PASS', 'stack_depth': 3}, {'op': 'OP_HASH160', 'result': 'PASS', 'hash': '4f1f14899c66c1b7d41c1bfec2158ea969ddf8d1', 'stack_depth': 3}, {'op': 'PUSH', 'value': '4f1f14899c66c1b7d41c1bfec2158ea969ddf8d1', 'stack_depth': 4}, {'op': 'OP_EQUALVERIFY', 'result': 'PASS', 'stack_depth': 2}, {'op': 'OP_CHECKSIG', 'result': 'PASS', 'stack_depth': 1}], 'z': 'e4c51f8c2c505d8b6fc40d27a7a557723a531bb590b7157b30d349c104e9230e', 'input_index': 0, 'segwit': False}

[ PASS ] tests.test_pipeline_full

============================================================
[ RUNNING ] tests.test_schnorr_verify
============================================================
SCHNORR VERIFY RESULT: False

[ PASS ] tests.test_schnorr_verify

============================================================
[ RUNNING ] tests.test_script_type
============================================================
P2SH: {'type': 'P2SH', 'pubkey_hash': '3333333333333333333333333333333333333333'}
P2TR: {'type': 'P2TR', 'pubkey_hash': '4444444444444444444444444444444444444444444444444444444444444444'}
P2PKH: {'type': 'P2PKH', 'pubkey_hash': '1111111111111111111111111111111111111111'}
P2WPKH: {'type': 'P2WPKH', 'pubkey_hash': '2222222222222222222222222222222222222222'}
UNKNOWN: {'type': 'UNKNOWN', 'pubkey_hash': None}
P2WPKH scriptCode: 76a914222222222222222222222222222222222222222288ac

[ PASS ] tests.test_script_type

============================================================
[ RUNNING ] tests.test_compressed_pubkey
============================================================
>>> PUSH 3045022053516769a331669ec971334d787e66ad43f8d42982e9838b1e8b8241514b8fff022100a81c6a31473dac9b8b6696f5273742d8f56b90beaa64cc908f2b7ff06dcdcf4301
>>> PUSH 02c558a36a91a0a23c125fd3fc2376ac0bdc87557bfc94d4f022d8c79eeba49ab5
>>> OP_DUP
>>> OP_HASH160
>>> PUSH 99dc70fc537968c3935f484bc22ad8e432e1f117
>>> OP_EQUALVERIFY
[ EQUALVERIFY SUCCESS ]
>>> OP_CHECKSIG

[ SCRIPT SUCCESS ]

STACK:
0: True
COMPRESSED PUBKEY: 02c558a36a91a0a23c125fd3fc2376ac0bdc87557bfc94d4f022d8c79eeba49ab5
PUBKEY HASH: 99dc70fc537968c3935f484bc22ad8e432e1f117
{'type': 'P2PKH', 'valid': True, 'script_result': 'PASS', 'engine': 'Arkeon Core Validator', 'trace': [{'op': 'PUSH', 'value': '3045022053516769a331669ec971334d787e66ad43f8d42982e9838b1e8b8241514b8fff022100a81c6a31473dac9b8b6696f5273742d8f56b90beaa64cc908f2b7ff06dcdcf4301', 'stack_depth': 1}, {'op': 'PUSH', 'value': '02c558a36a91a0a23c125fd3fc2376ac0bdc87557bfc94d4f022d8c79eeba49ab5', 'stack_depth': 2}, {'op': 'OP_DUP', 'result': 'PASS', 'stack_depth': 3}, {'op': 'OP_HASH160', 'result': 'PASS', 'hash': '99dc70fc537968c3935f484bc22ad8e432e1f117', 'stack_depth': 3}, {'op': 'PUSH', 'value': '99dc70fc537968c3935f484bc22ad8e432e1f117', 'stack_depth': 4}, {'op': 'OP_EQUALVERIFY', 'result': 'PASS', 'stack_depth': 2}, {'op': 'OP_CHECKSIG', 'result': 'PASS', 'stack_depth': 1}]}

[ PASS ] tests.test_compressed_pubkey

============================================================
[ RUNNING ] tests.test_router
============================================================

P2PKH API TEST DATA:
RAW_TX: 02000000010000000000000000000000000000000000000000000000000000000000000000000000008a473044022060b8ecbd433f072481d50c38943dbdb1af6cef4fb7b37d31216639a1b5f28d4f0220098a4363dcf09a14b21fbc94626e4b5fe0deec131bc64267b90f27de1294a969014104fedf5a63ad83732968c7293d1bdda5cb967c484db1410df7ac52ff342145bc6e161f7e7523e50ee1889b11ca81de6e1add69ede26502a5f08492b952e4a7a86dffffffff0198ecfa02000000001976a914e5ea4ebe722fa3227e6bc93acf65e6c97eba16e088ac00000000
SCRIPT_PUBKEY: 76a914e5ea4ebe722fa3227e6bc93acf65e6c97eba16e088ac
AMOUNT: 50000000
>>> PUSH 3044022060b8ecbd433f072481d50c38943dbdb1af6cef4fb7b37d31216639a1b5f28d4f0220098a4363dcf09a14b21fbc94626e4b5fe0deec131bc64267b90f27de1294a96901
>>> PUSH 04fedf5a63ad83732968c7293d1bdda5cb967c484db1410df7ac52ff342145bc6e161f7e7523e50ee1889b11ca81de6e1add69ede26502a5f08492b952e4a7a86d
>>> OP_DUP
>>> OP_HASH160
>>> PUSH e5ea4ebe722fa3227e6bc93acf65e6c97eba16e0
>>> OP_EQUALVERIFY
[ EQUALVERIFY SUCCESS ]
>>> OP_CHECKSIG

[ SCRIPT SUCCESS ]

STACK:
0: True
TAPROOT DEBUG: P2PKH P2PKH False
PROFILE FINGERPRINT: 9bf4cf0b7419ff78
PROFILE OCCURRENCES: 509

P2PKH ROUTER RESULT:
{'type': 'P2PKH', 'valid': True, 'script_result': 'PASS', 'engine': 'Arkeon Core Validator', 'trace': [{'op': 'PUSH', 'value': '3044022060b8ecbd433f072481d50c38943dbdb1af6cef4fb7b37d31216639a1b5f28d4f0220098a4363dcf09a14b21fbc94626e4b5fe0deec131bc64267b90f27de1294a96901', 'stack_depth': 1}, {'op': 'PUSH', 'value': '04fedf5a63ad83732968c7293d1bdda5cb967c484db1410df7ac52ff342145bc6e161f7e7523e50ee1889b11ca81de6e1add69ede26502a5f08492b952e4a7a86d', 'stack_depth': 2}, {'op': 'OP_DUP', 'result': 'PASS', 'stack_depth': 3}, {'op': 'OP_HASH160', 'result': 'PASS', 'hash': 'e5ea4ebe722fa3227e6bc93acf65e6c97eba16e0', 'stack_depth': 3}, {'op': 'PUSH', 'value': 'e5ea4ebe722fa3227e6bc93acf65e6c97eba16e0', 'stack_depth': 4}, {'op': 'OP_EQUALVERIFY', 'result': 'PASS', 'stack_depth': 2}, {'op': 'OP_CHECKSIG', 'result': 'PASS', 'stack_depth': 1}], 'z': '10b588dd9842af065de23bfb706e13bd5bd11ea45114738fa8c906ec36ba8b02', 'input_index': 0, 'segwit': False, 'router': 'UniversalValidator', 'detected_type': 'P2PKH', 'display_type': 'Legacy P2PKH', 'txid': '7e1ee5c6e722caed4545478d013fd89ab04b70aea0f8056aa2bc7ebedaf84225', 'risk': {'risk_level': 'LOW', 'risk_score': 0, 'flags': ['CONSENSUS_VALID'], 'summary': 'P2PKH transaction appears normal under active Arkeon validation rules.'}, 'policy': {'policy_action': 'ALLOW', 'policy_score': 0, 'policy_flags': [], 'summary': 'P2PKH transaction is acceptable under the current Arkeon policy profile.'}, 'anomaly': {'anomaly_detected': False, 'severity': 'NORMAL', 'signals': [], 'signal_count': 0, 'summary': 'No abnormal transaction behavior was detected under the active Arkeon anomaly profile.'}, 'taproot_intelligence': {'taproot_active': False, 'annex_present': False, 'complexity': 'LOW', 'tapleaf_depth': 0, 'branch_count': 1, 'execution_path_type': 'KEY_OR_SINGLE_BRANCH', 'sighash_type': 'DEFAULT', 'sighash_profile': 'DEFAULT_PROFILE', 'anyonecanpay': False, 'complexity_score': 5, 'signals': ['CONSENSUS_VALIDATED', 'DEFAULT_SIGHASH_PROFILE'], 'summary': 'Transaction is not currently classified as Taproot by the active router.'}, 'historical_intelligence': {'fingerprint': '9bf4cf0b7419ff78', 'tx_fingerprint': '7b2d6a3e373eed11', 'profile': 'P2PKH|0|DEFAULT_PROFILE|KEY_OR_SINGLE_BRANCH|0|0|0|0|0|0|0', 'classification': 'STANDARD_PROFILE', 'summary': 'Transaction fingerprint 9bf4cf0b7419ff78 classified as STANDARD_PROFILE.'}, 'historical_memory': {'stored': True, 'fingerprint': '9bf4cf0b7419ff78', 'repeat_count': 509, 'memory_status': 'REPEATED_BEHAVIOR_PROFILE'}}

P2WPKH API TEST DATA:
RAW_TX: 0200000000010111111111111111111111111111111111111111111111111111111111111111110000000000ffffffff01d864780400000000160014aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa02483045022100fdec4391bad443b12332d43a7e91185cf017eada248343e19333b4b44c0ff67002200b71e29f9aa43e74e9c29fd82bf8557f6aa1e30ec51c18d5a91f6810618d1adb01410431c7bc064b87059b32d0399754f35a681467241bf78f8263a6c3f5a7b4edf430f9993254c0e4369c4b6c2bb174eaacec36ec6b3369a2e1b4f818b4ad99f7420e00000000
SCRIPT_PUBKEY: 0014dd35793383c20131eec11ba6b8dcf729d5472884
AMOUNT: 75000000
>>> PUSH 3045022100fdec4391bad443b12332d43a7e91185cf017eada248343e19333b4b44c0ff67002200b71e29f9aa43e74e9c29fd82bf8557f6aa1e30ec51c18d5a91f6810618d1adb01
>>> PUSH 0431c7bc064b87059b32d0399754f35a681467241bf78f8263a6c3f5a7b4edf430f9993254c0e4369c4b6c2bb174eaacec36ec6b3369a2e1b4f818b4ad99f7420e
>>> OP_DUP
>>> OP_HASH160
>>> PUSH dd35793383c20131eec11ba6b8dcf729d5472884
>>> OP_EQUALVERIFY
[ EQUALVERIFY SUCCESS ]
>>> OP_CHECKSIG

[ SCRIPT SUCCESS ]

STACK:
0: True
TAPROOT DEBUG: P2WPKH P2WPKH False
PROFILE FINGERPRINT: d51b71c23ac3de83
PROFILE OCCURRENCES: 8383

P2WPKH ROUTER RESULT:
{'type': 'P2WPKH', 'valid': True, 'script_result': 'PASS', 'engine': 'Arkeon Core Validator', 'trace': [{'op': 'PUSH', 'value': '3045022100fdec4391bad443b12332d43a7e91185cf017eada248343e19333b4b44c0ff67002200b71e29f9aa43e74e9c29fd82bf8557f6aa1e30ec51c18d5a91f6810618d1adb01', 'stack_depth': 1}, {'op': 'PUSH', 'value': '0431c7bc064b87059b32d0399754f35a681467241bf78f8263a6c3f5a7b4edf430f9993254c0e4369c4b6c2bb174eaacec36ec6b3369a2e1b4f818b4ad99f7420e', 'stack_depth': 2}, {'op': 'OP_DUP', 'result': 'PASS', 'stack_depth': 3}, {'op': 'OP_HASH160', 'result': 'PASS', 'hash': 'dd35793383c20131eec11ba6b8dcf729d5472884', 'stack_depth': 3}, {'op': 'PUSH', 'value': 'dd35793383c20131eec11ba6b8dcf729d5472884', 'stack_depth': 4}, {'op': 'OP_EQUALVERIFY', 'result': 'PASS', 'stack_depth': 2}, {'op': 'OP_CHECKSIG', 'result': 'PASS', 'stack_depth': 1}], 'z': '981150205d62e2b5a039ac8cd865dce64dfd281b704dbfafd904fc4abb0e1ffb', 'input_index': 0, 'segwit': True, 'witness_items': 2, 'router': 'UniversalValidator', 'detected_type': 'P2WPKH', 'display_type': 'Native SegWit P2WPKH', 'txid': '51d6c97f02b387c27fe1d6e3da217df6010813e3cb61c7144a3660070f46817a', 'risk': {'risk_level': 'LOW', 'risk_score': 0, 'flags': ['CONSENSUS_VALID'], 'summary': 'P2WPKH transaction appears normal under active Arkeon validation rules.'}, 'policy': {'policy_action': 'ALLOW', 'policy_score': 0, 'policy_flags': [], 'summary': 'P2WPKH transaction is acceptable under the current Arkeon policy profile.'}, 'anomaly': {'anomaly_detected': False, 'severity': 'NORMAL', 'signals': [], 'signal_count': 0, 'summary': 'No abnormal transaction behavior was detected under the active Arkeon anomaly profile.'}, 'taproot_intelligence': {'taproot_active': False, 'annex_present': False, 'complexity': 'LOW', 'tapleaf_depth': 0, 'branch_count': 1, 'execution_path_type': 'KEY_OR_SINGLE_BRANCH', 'sighash_type': 'DEFAULT', 'sighash_profile': 'DEFAULT_PROFILE', 'anyonecanpay': False, 'complexity_score': 25, 'signals': ['SCRIPT_PATH_OR_EXTENDED_WITNESS_PROFILE', 'CONSENSUS_VALIDATED', 'DEFAULT_SIGHASH_PROFILE'], 'summary': 'Transaction is not currently classified as Taproot by the active router.'}, 'historical_intelligence': {'fingerprint': 'd51b71c23ac3de83', 'tx_fingerprint': '18a2044c68ddb7f7', 'profile': 'P2WPKH|2|DEFAULT_PROFILE|KEY_OR_SINGLE_BRANCH|0|0|0|0|0|0|0', 'classification': 'STANDARD_PROFILE', 'summary': 'Transaction fingerprint d51b71c23ac3de83 classified as STANDARD_PROFILE.'}, 'historical_memory': {'stored': True, 'fingerprint': 'd51b71c23ac3de83', 'repeat_count': 8383, 'memory_status': 'REPEATED_BEHAVIOR_PROFILE'}}

[ ROUTER TEST PASSED ]

[ PASS ] tests.test_router

============================================================
[ RUNNING ] tests.test_p2wpkh_pipeline
============================================================

RAW SEGWIT TX:
0200000000010111111111111111111111111111111111111111111111111111111111111111110000000000ffffffff01d864780400000000160014aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa024930460221009a6044ee4a2592df187cb9e5057521d73291d2bfc007f0e290a0c7a289e7db68022100edc2e84d6ae511e0e18b66f6fb33b4bfda59ec48697c6a79906be8a963a4a8c1014104dafd768daaa9f968ee503204c585b2c8e859d81c37c014ce1c8c869c4822ecafd1f19550928a871c326d234602eb5b2616059a65084dcd1521d9c55e8e54d74300000000

BUILDER Z:
1e68818603a037657b63a14f14a7d05c643bdcea1aa8b3b46d1aeb3630903681

SCRIPT CODE:
76a91438375c2d2b860a3cfb3aa9b1d4e5ee7dd089e0c988ac
>>> PUSH 30460221009a6044ee4a2592df187cb9e5057521d73291d2bfc007f0e290a0c7a289e7db68022100edc2e84d6ae511e0e18b66f6fb33b4bfda59ec48697c6a79906be8a963a4a8c101
>>> PUSH 04dafd768daaa9f968ee503204c585b2c8e859d81c37c014ce1c8c869c4822ecafd1f19550928a871c326d234602eb5b2616059a65084dcd1521d9c55e8e54d743
>>> OP_DUP
>>> OP_HASH160
>>> PUSH 38375c2d2b860a3cfb3aa9b1d4e5ee7dd089e0c9
>>> OP_EQUALVERIFY
[ EQUALVERIFY SUCCESS ]
>>> OP_CHECKSIG

[ SCRIPT SUCCESS ]

STACK:
0: True

PIPELINE RESULT:
{'type': 'P2WPKH', 'valid': True, 'script_result': 'PASS', 'engine': 'Arkeon Core Validator', 'trace': [{'op': 'PUSH', 'value': '30460221009a6044ee4a2592df187cb9e5057521d73291d2bfc007f0e290a0c7a289e7db68022100edc2e84d6ae511e0e18b66f6fb33b4bfda59ec48697c6a79906be8a963a4a8c101', 'stack_depth': 1}, {'op': 'PUSH', 'value': '04dafd768daaa9f968ee503204c585b2c8e859d81c37c014ce1c8c869c4822ecafd1f19550928a871c326d234602eb5b2616059a65084dcd1521d9c55e8e54d743', 'stack_depth': 2}, {'op': 'OP_DUP', 'result': 'PASS', 'stack_depth': 3}, {'op': 'OP_HASH160', 'result': 'PASS', 'hash': '38375c2d2b860a3cfb3aa9b1d4e5ee7dd089e0c9', 'stack_depth': 3}, {'op': 'PUSH', 'value': '38375c2d2b860a3cfb3aa9b1d4e5ee7dd089e0c9', 'stack_depth': 4}, {'op': 'OP_EQUALVERIFY', 'result': 'PASS', 'stack_depth': 2}, {'op': 'OP_CHECKSIG', 'result': 'PASS', 'stack_depth': 1}], 'z': '1e68818603a037657b63a14f14a7d05c643bdcea1aa8b3b46d1aeb3630903681', 'input_index': 0, 'segwit': True, 'witness_items': 2}

[ PASS ] tests.test_p2wpkh_pipeline

############################################################
[ SUMMARY ] 26/26 tests passed
############################################################

[ ARKEON STATUS ] CONSENSUS STABLE
