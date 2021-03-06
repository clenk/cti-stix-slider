STIX Slider Log Messages
==========================

Use the following table for reference. You can also enable or disable certain
messages using the ``-e`` or ``-d`` flags. Refer to the elevator help
or README for more information on how to handle logging messages.

=================================================================================================================== =========================================================== ====    =====   ===================================================================
Message                                                                                                             Category                                                    Code    Level   Location
=================================================================================================================== =========================================================== ====    =====   ===================================================================
Observable Expressions should not contain placeholders                                                              General                                                     201     Error   ObservableExpressionForElevator.contains_placeholder
Both console and output log have disabled messages                                                                  General                                                     202     Warn    initialize_options
silent option is not compatible with a policy                                                                       General                                                     203     Warn    initialize_options
options not initialized                                                                                             General                                                     204     Warn    set_option_value
No source object exists for [id] to add the relationship [relationship]                                             Possible issue in original STIX 2.0 content                 301     Warn    process_relationships
Unknown hash type [hash_type] used in [id]                                                                          Possible issue in original STIX 2.0 content                 302     Warn    add_hashes_property
[property] is not a legal property in the pattern of [id]                                                           Possible issue in original STIX 2.0 content                 303     Warn    *many* in convert_pattern.py
Unknown address type [type] used in [id]                                                                            Possible issue in original STIX 2.0 content                 304     Warn    convert_addr_pattern
No object [id] is found to add the reference to                                                                     Possible issue in original STIX 2.0 content                 305     Warn    create_references
[cyber_observable_id] is not an index found in [id]                                                                 Possible issue in original STIX 2.0 content                 306     Warn    *many* in convert_cyber_observables.py
No object [id] is found to add the reference to                                                                     Possible issue in original STIX 2.0 content                 307     Warn    create_references
[id1] is not in this bundle.  Referenced from [id2]                                                                 Possible issue in original STIX 2.0 content                 308     Warn    process_sighting
is_encrypted in [id] is true, but no encryption_algorithm is given                                                  Possible issue in original STIX 2.0 content                 309     Info    convert_file_c_o
is_encrypted in [id] is false, but encryption_algorithm is given                                                    Possible issue in original STIX 2.0 content                 310     Info    convert_file_c_o
is_encrypted in %s is true, but no decryption_key is given                                                          Possible issue in original STIX 2.0 content                 311     Info    convert_file_c_o
is_encrypted in %s is false, but decryption_key is given                                                            Possible issue in original STIX 2.0 content                 312     Info    convert_file_c_o
The is_multipart property in [id] should be 'true' if the body_multipart property is present                        Possible issue in original STIX 2.0 content                 313     Warn    convert_email_message_c_o
The is_multipart property in [id] should be 'false' if the body_multipart property is not present                   Possible issue in original STIX 2.0 content                 314     Warn    convert_email_message_c_o
[type] in STIX 2.0 has multiple [property], only one is allowed in STIX 1.x. Using first in list - [value] omitted  Multiple values are not supported in STIX 1.x               401     Warn    convert_coa, convert_identity, populate_other_header_fields
Only one dll can be represented in STIX 1.x for [id], using first one - ignoring [value]                            Multiple values are not supported in STIX 1.x               402     Warn    add_process_extension_pattern
The [relationship] relationship between [id1] and [id2] is not supported in STIX 1.x"                               Content not supported in STIX 1.x - Dropping                501     Warn    get_relationship_adder
Multiple File Extensions in [id] not supported yet                                                                  Content not supported in STIX 1.x - Dropping                502     Warn    determine_1x_object_type
[property] not representable in a STIX 1.x [type].  Found in [id]                                                   Content not supported in STIX 1.x - Dropping                503     Warn    convert_image_file_extension
[property] not representable in a STIX 1.x [type].  Found in the pattern of [id]                                    Content not supported in STIX 1.x - Dropping                504     Warn    add_scalar_process_property_pattern,
                                                                                                                                                                                                add_list_process_property_pattern,
                                                                                                                                                                                                add_scalar_registry_key_property_pattern
[op] cannot be converted to a STIX 1.x operator in the pattern of [id]                                              Content not supported in STIX 1.x - Dropping                505     Warn    convert_operator
account_type property of [id] in STIX 2.0 is not directly represented as a property in STIX 1.x                     Content not supported in STIX 1.x - Dropping                506     Warn    convert_user_account_pattern
Received Line [line] in [id] has a prefix that is not representable in STIX 1.x                                     Content not supported in STIX 1.x - Dropping                507     Warn    populate_received_line
Unable to convert STIX 2.0 sighting [id] because it doesn't refer to an indicator                                   Content not supported in STIX 1.x - Dropping                508     Warn    convert_sighting
Cannot convert STIX 2.0 content that contains intrusion-sets                                                        Content not supported in STIX 1.x - Dropping                509     Warn    convert_bundle
Identity has no property to store external-references from [id]                                                     Content not supported in STIX 1.x - Dropping                510     Warn    create_references
pe_type SYS in [id] is valid in STIX 2.0, but not in STIX 1.x                                                       Content not supported in STIX 1.x - Dropping                511     Warn    convert_pe_type
pe_type [pe_type] in [id] is allowed in STIX 2.0, but not in STIX 1.x                                               Content not supported in STIX 1.x - Dropping                512     Warn    convert_pe_type
[property] is an XML attribute of [cybox object type] in STIX 1.x, so the operator 'equals' is assumed in [id]      Content not supported in STIX 1.x - Dropping                513     Warn    add_scalar_artifact_property_pattern
Order may not be maintained for pdfids in [id]                                                                      Content not supported in STIX 1.x - Dropping                514     Warn    add_file_pdf_extension_pattern
The 'groups' property of unix-account-ext contains strings, but the STIX 1.x property expects integers in %s        Content not supported in STIX 1.x - Dropping                515     Warn    convert_unix_account_extensions
No file name provided for binary_ref of [id], therefore it cannot be represented in the STIX 1.x Process object     Content not supported in STIX 1.x - Dropping                516     Warn    convert_process_c_o
Hashes of the binary_ref of [id] process cannot be represented in the STIX 1.x Process object                       Content not supported in STIX 1.x - Dropping                517     Warn    convert_process_c_o
resolves_to_refs in [id] not representable in STIX 1.x                                                              Content not supported in STIX 1.x - Dropping                518     Warn    convert_domain_name_c_o
Multiple Network Traffic extensions in [id] not supported yet                                                       Content not supported in STIX 1.x - Dropping                519     Warn    determine_1x_object_type
The user_id property of [id] in STIX 2.0 is only represented as a property in STIX 1.x on UnixUserAccount objects   Content not supported in STIX 1.x - Dropping                520     Warn    convert_user_account_pattern
The [property] property in [id] can refer to any object, so it is not handled yet.                                  STIX slider currently doesn't process this content          601     Warn    add_list_file_property_pattern
number indicies in [id] not handled, yet                                                                            STIX slider currently doesn't process this content          602     Warn    *many* in convert_pattern.py
Unable to determine STIX 1.x type for [id]                                                                          STIX slider currently doesn't process this content          603     Error   convert_cyber_observable
Granular Markings present in [id] are not supported by stix2slider                                                  STIX slider currently doesn't process this content          604     Warn    *many* in convert_stix.py
Source name [name] in external references of [id] not handled, yet                                                  STIX slider currently doesn't process this content          605     Warn    create_references
[property] property in [id] not handled yet                                                                         STIX slider currently doesn't process this content          606     Warn    convert_add_c_o
contains_refs in [id] not handled                                                                                   STIX slider currently doesn't process this content          607     Warn    convert_file_c_o
protocols property in [id] not handled, yet                                                                         STIX slider currently doesn't process this content          608     Warn    convert_network_traffic_c_o
tcp-ext in [id] not handled, yet                                                                                    STIX slider currently doesn't process this content          609     Warn    convert_network_traffic_to_tcp_packet
                                                                                                                                                                                                convert_network_packet_pattern
Assuming imcp packet in [id] is v4                                                                                  Processing based on assumptions                             701     Info    convert_network_traffic_to_icmp_packet
=================================================================================================================== =========================================================== ====    =====   ===================================================================

