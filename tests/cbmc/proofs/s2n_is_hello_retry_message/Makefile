# Copyright Amazon.com, Inc. or its affiliates. All Rights Reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License"). You may not use
# this file except in compliance with the License. A copy of the License is
# located at
#
#     http://aws.amazon.com/apache2.0/
#
# or in the "license" file accompanying this file. This file is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
# implied. See the License for the specific language governing permissions and
# limitations under the License.

# Use the default set of CBMC flags.
CBMCFLAGS +=

PROOF_UID = s2n_is_hello_retry_message
HARNESS_ENTRY = $(PROOF_UID)_harness
HARNESS_FILE = $(HARNESS_ENTRY).c

PROOF_SOURCES += $(PROOFDIR)/$(HARNESS_FILE)
PROOF_SOURCES += $(PROOF_STUB)/s2n_calculate_stacktrace.c

PROJECT_SOURCES += $(SRCDIR)/tls/s2n_handshake_io.c
PROJECT_SOURCES += $(SRCDIR)/tls/s2n_handshake.c
PROJECT_SOURCES += $(SRCDIR)/utils/s2n_result.c

UNWINDSET +=

include ../Makefile.common
