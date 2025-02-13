# finite-state-rice-decoder
Java implementation of byte-level finite state decoder for a stream of Rice codes with constant space complexity with respect to alphabet size.

Finite-state machine implementation is done using Enum types (see State.java). The conventional bit-level decoding procedure is also implemented (see BitLevelDecoder.java). Finite-state decoding, which decodes variable length Rice codes bytewise, is faster and comparatively becomes more effective as the mean value of encoded integers increases. Speed gains up to a factor of 2 have empirically been observed in an inverted index compression task where document gaps are geometrically distributed (approximately) under the assumption that documents are randomly ordered.

The unary part is encoded as 0's followed by a 1 in this implementation.

The paper that describes and evaluates the finite-state decoder can be found at https://www.researchgate.net/publication/344635127_Efficient_Finite-State_Decoding_of_Rice_Codes_for_Large_Alphabets
