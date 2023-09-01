#
# Copyright (C) 2011-2021 Intel Corporation. All rights reserved.
#
# Redistribution and use in source and binary forms, with or without
# modification, are permitted provided that the following conditions
# are met:
#
#   * Redistributions of source code must retain the above copyright
#     notice, this list of conditions and the following disclaimer.
#   * Redistributions in binary form must reproduce the above copyright
#     notice, this list of conditions and the following disclaimer in
#     the documentation and/or other materials provided with the
#     distribution.
#   * Neither the name of Intel Corporation nor the names of its
#     contributors may be used to endorse or promote products derived
#     from this software without specific prior written permission.
#
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
# "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
# LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
# A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
# OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
# SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
# LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
# DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
# THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
# (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
# OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
#
#

include ../../../buildenv.mk

CXXFLAGS += -Werror -USE_DEBUG_LEVEL -DSE_DEBUG_LEVEL=SE_TRACE_DEBUG
CFLAGS   += -Werror -USE_DEBUG_LEVEL -DSE_DEBUG_LEVEL=SE_TRACE_DEBUG

CFLAGS += -g -O0 -fpie -DOPENSSL_API_COMPAT=10101 -DHAVE_THREAD_LS -DNDEBUG -DNO_DO178 -DWOLFSSL_X86_64_BUILD -DHAVE_LIBOQS -DHAVE_TLS_EXTENSIONS -pthread -DERROR_QUEUE_PER_THREAD -DTFM_TIMING_RESISTANT -DECC_TIMING_RESISTANT -DWC_RSA_BLINDING -DWOLFSSL_USE_ALIGN -DWOLFSSL_SHA224 -DWOLFSSL_SHA512 -DWOLFSSL_SHA384 -DHAVE_HKDF -DNO_DSA -DHAVE_ECC -DTFM_ECC256 -DECC_SHAMIR -DHAVE_ECC_ENCRYPT -DWC_RSA_PSS -DWOLFSSL_PSS_LONG_SALT -DWOLFSSL_BASE64_ENCODE -DWOLFSSL_SHA3 -DWOLFSSL_NO_SHAKE128 -DWOLFSSL_NO_SHAKE256 -DHAVE_POLY1305 -DHAVE_CHACHA -DHAVE_HASHDRBG -DHAVE_TLS_EXTENSIONS -DHAVE_SUPPORTED_CURVES -DHAVE_FFDHE_2048 -DHAVE_SUPPORTED_CURVES -DWOLFSSL_TLS13 -DHAVE_TLS_EXTENSIONS -DHAVE_EXTENDED_MASTER -DNO_RC4 -DHAVE_ENCRYPT_THEN_MAC -DNO_PSK -DNO_MD4 -DWOLFSSL_SP_MATH_ALL -DWOLFSSL_SP_X86_64 -DWC_NO_ASYNC_THREADING -DHAVE_DH_DEFAULT_PARAMS -DWOLFSSL_SYS_CA_CERTS -DWOLFSSL_CERT_REQ -DWOLFSSL_CERT_GEN -DWOLFSSL_CERT_EXT -DNO_DES3 -DGCM_TABLE_4BIT -DHAVE_AESGCM -DHAVE_TLS_EXTENSIONS -DHAVE_SERVER_RENEGOTIATION_INFO -Wall -Wno-unused -O2 -DHAVE___UINT128_T=1 -DWOLFSSL_TEST_STATIC_BUILD -DHAVE_WC_INTROSPECTION
CXXFLAGS += -g -O0 -fpie -DOPENSSL_API_COMPAT=10101 -DHAVE_THREAD_LS -DNDEBUG -DNO_DO178 -DWOLFSSL_X86_64_BUILD -DHAVE_LIBOQS -DHAVE_TLS_EXTENSIONS -pthread -DERROR_QUEUE_PER_THREAD -DTFM_TIMING_RESISTANT -DECC_TIMING_RESISTANT -DWC_RSA_BLINDING -DWOLFSSL_USE_ALIGN -DWOLFSSL_SHA224 -DWOLFSSL_SHA512 -DWOLFSSL_SHA384 -DHAVE_HKDF -DNO_DSA -DHAVE_ECC -DTFM_ECC256 -DECC_SHAMIR -DHAVE_ECC_ENCRYPT -DWC_RSA_PSS -DWOLFSSL_PSS_LONG_SALT -DWOLFSSL_BASE64_ENCODE -DWOLFSSL_SHA3 -DWOLFSSL_NO_SHAKE128 -DWOLFSSL_NO_SHAKE256 -DHAVE_POLY1305 -DHAVE_CHACHA -DHAVE_HASHDRBG -DHAVE_TLS_EXTENSIONS -DHAVE_SUPPORTED_CURVES -DHAVE_FFDHE_2048 -DHAVE_SUPPORTED_CURVES -DWOLFSSL_TLS13 -DHAVE_TLS_EXTENSIONS -DHAVE_EXTENDED_MASTER -DNO_RC4 -DHAVE_ENCRYPT_THEN_MAC -DNO_PSK -DNO_MD4 -DWOLFSSL_SP_MATH_ALL -DWOLFSSL_SP_X86_64 -DWC_NO_ASYNC_THREADING -DHAVE_DH_DEFAULT_PARAMS -DWOLFSSL_SYS_CA_CERTS -DWOLFSSL_CERT_REQ -DWOLFSSL_CERT_GEN -DWOLFSSL_CERT_EXT -DNO_DES3 -DGCM_TABLE_4BIT -DHAVE_AESGCM -DHAVE_TLS_EXTENSIONS -DHAVE_SERVER_RENEGOTIATION_INFO -Wall -Wno-unused -O2 -DHAVE___UINT128_T=1 -DWOLFSSL_TEST_STATIC_BUILD -DHAVE_WC_INTROSPECTION
LDFLAGS := -pie $(COMMON_LDFLAGS)

INC += $(ADDED_INC)
INC +=  -I$(COMMON_DIR)/inc                         \
        -I$(COMMON_DIR)/inc/internal                \
        -I$(COMMON_DIR)/inc/internal/linux/         \
        -I$(LINUX_PSW_DIR)/enclave_common           \
        -I$(LINUX_PSW_DIR)/urts                     \
        -I$(LINUX_PSW_DIR)/urts/linux               \
        -I$(LINUX_PSW_DIR)/urts/parser              \
        -I/home/mspiegel/git/mesh-process/c-libraries/install/wolfssl-app/include

DIR2 := $(COMMON_DIR)/src/
DIR3 := $(LINUX_PSW_DIR)/urts/
DIR4 := $(LINUX_PSW_DIR)/urts/linux
DIR5 := $(LINUX_PSW_DIR)/urts/parser
DIR6 := $(LINUX_PSW_DIR)/psw/urts/parser/linux

OBJ1 := manage_metadata.o      \
        enclave_creator_sign.o \
        sign_tool.o            \
        util_st.o

OBJ2 := sgx_memset_s.o

OBJ4 := loader.o     \
        se_detect.o  

CPP_OBJS := $(OBJ1) $(OBJ2) $(OBJ4)
C_OBJS   := se_trace.o se_map.o
OBJS     := $(CPP_OBJS) $(C_OBJS)

vpath %.cpp $(DIR2):$(DIR3):$(DIR4):$(DIR5):$(DIR6)

.PHONY: all
all: sgx_sign | $(BUILD_DIR)
	@$(CP) $< $|

$(BUILD_DIR):
	@$(MKDIR) $@

sgx_sign: PRIVATE_LDLIBS  := -lpthread -lenclaveparser -lwolfssl -loqs
sgx_sign: PRIVATE_LDFLAGS := -L$(LINUX_PSW_DIR)/urts/parser \
	                     -L/home/mspiegel/git/mesh-process/c-libraries/install/wolfssl-app/lib \
	                     -L/home/mspiegel/git/mesh-process/c-libraries/install/oqs-app/lib \
			     $(LDFLAGS)

sgx_sign: $(OBJS) enclaveparser
	$(CXX) $(CXXFLAGS) $(OBJS) $(PRIVATE_LDFLAGS) $(PRIVATE_LDLIBS) -o $@

$(CPP_OBJS): %.o: %.cpp
	$(CXX) $(CXXFLAGS) $(INC) -c $< -o $@

$(C_OBJS):   %.o: $(DIR2)%.c
	$(CC) $(CFLAGS) $(INC) -c $< -o $@

.PHONY: clean
clean:
	$(RM) *~ *.o sgx_sign $(BUILD_DIR)/sgx_sign
	$(MAKE) -C $(LINUX_PSW_DIR)/urts/parser/ clean

.PHONY: enclaveparser
enclaveparser:
	$(MAKE) -C $(LINUX_PSW_DIR)/urts/parser/ SIGN_TOOL=1
