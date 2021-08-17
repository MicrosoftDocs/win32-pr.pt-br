---
description: Usado com as funções BCryptGetProperty e BCryptSetProperty para identificar uma propriedade.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Identificadores de propriedade primitiva de criptografia (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5452c6a55388998a08577cb19ef2fba6905faddbdf28f5f8051b7bc8d9d1c375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908217"
---
# <a name="cryptography-primitive-property-identifiers"></a>Identificadores de propriedade primitiva de criptografia

Os valores a seguir são usados com as funções [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) e [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) para identificar uma propriedade.

<dl> <dt>

<span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**NOME DO ALGORITMO BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"AlgorithmName"
</dt> <dt>



Uma cadeia de caracteres Unicode terminada em nulo que contém o nome do algoritmo.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**COMPRIMENTO DA \_ MARCA DE AUTH BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"AuthTagLength"
</dt> <dt>



Os comprimentos da marca de autenticação com suporte pelo algoritmo. Essa propriedade é uma [**estrutura \_ \_ \_ \_ STRUCT BCRYPT AUTH TAG LENGTHS.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) Essa propriedade se aplica somente a algoritmos.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**COMPRIMENTO DO BLOCO BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"BlockLength"
</dt> <dt>



O tamanho, em bytes, de um bloco de criptografia para o algoritmo. Essa propriedade só se aplica a algoritmos de criptografia de bloco. Esse tipo de dados é **um DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**BCRYPT \_ BLOCK \_ SIZE \_ LIST**
</dt> <dd> <dl> <dt>

L"BlockSizeList"
</dt> <dt>



Uma lista dos comprimentos de bloco com suporte por um algoritmo de criptografia. Esse tipo de dados é uma matriz **de DWORDs.** O número de elementos na matriz pode ser determinado dividindo o número de bytes recuperados pelo tamanho de um **único DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**MODO DE \_ ENCADEAMENTO \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"ChainingMode"
</dt> <dt>



Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que representa o modo de encadeamento do algoritmo de criptografia. Essa propriedade pode ser definida em um alça de algoritmo ou um alça de chave para um dos valores a seguir.



| Identificador                   | Valor                         | Descrição                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BCRYPT \_ CHAIN \_ MODE \_ CBC** | L"ChainingModeCBC"<br/> | Define o modo de encadeamento do algoritmo como [*encadeamento de blocos de criptografia.*](/windows/desktop/SecGloss/c-gly)<br/>            |
| **\_CCM DO MODO CADEIA BCRYPT \_ \_** | L"ChainingModeCCM"<br/> | Define o modo de encadeamento do algoritmo para contador com o modo CBC-MAC (CCM). **Windows Vista:** Esse valor tem suporte a partir do Windows Vista com SP1.<br/> <br/> |
| **CFB DO MODO CADEIA BCRYPT \_ \_ \_** | L"ChainingModeCFB"<br/> | Define o modo de encadeamento do algoritmo como comentários [*de criptografia.*](/windows/desktop/SecGloss/c-gly)<br/>                              |
| **BCRYPT \_ CHAIN \_ MODE \_ ECB** | L"ChainingModeECB"<br/> | Define o modo de encadeamento do algoritmo para [*o codebook eletrônico*](/windows/desktop/SecGloss/e-gly).<br/>                  |
| **BCRYPT \_ CHAIN \_ MODE \_ GCM** | L"ChainingModeGCM"<br/> | Define o modo de encadeamento do algoritmo como GCM (modo de contador/de operação). **Windows Vista:** Esse valor tem suporte a partir do Windows Vista com SP1.<br/> <br/>       |
| **BCRYPT \_ CHAIN \_ MODE \_ NA**  | L"ChainingModeN/A"<br/> | O algoritmo não dá suporte ao encadeamento.<br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**PARÂMETROS \_ BCRYPT DH \_**
</dt> <dd> <dl> <dt>

L"DHParameters"
</dt> <dt>



Especifica os parâmetros a ser usado com uma Diffie-Hellman chave. Esse tipo de dados é um ponteiro para uma estrutura [**\_ BCRYPT DH \_ PARAMETER \_ HEADER.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Essa propriedade só pode ser definida e deve ser definida para a chave antes que a chave seja concluída.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**PARÂMETROS \_ BCRYPT \_ DSA**
</dt> <dd> <dl> <dt>

L"DSAParameters"
</dt> <dt>



Especifica parâmetros a usar com uma chave DSA. Essa propriedade é um [**HEADER \_ DE PARÂMETRO BCRYPT DSA \_ \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) ou uma estrutura [**BCRYPT \_ DSA \_ PARAMETER \_ HEADER \_ V2.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) Essa propriedade só pode ser definida e deve ser definida para a chave antes que a chave seja concluída.

**Windows 8:** Começando com Windows 8, essa propriedade pode ser uma estrutura [**BCRYPT \_ DSA \_ PARAMETER \_ HEADER \_ V2.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) Use essa estrutura se o tamanho da chave exceder 1024 bits e for menor ou igual a 3072 bits. Se o tamanho da chave for maior ou igual a 512, mas menor ou igual a 1024 bits, use a estrutura [**BCRYPT \_ DSA \_ PARAMETER \_ HEADER.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header)


</dt> </dl> </dd> <dt>

<span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**BCRYPT \_ EFFECTIVE \_ KEY \_ LENGTH**
</dt> <dd> <dl> <dt>

L"EffectiveKeyLength"
</dt> <dt>



O tamanho, em bits, do comprimento efetivo de uma chave RC2. Esse tipo de dados é **um DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**COMPRIMENTO DO BLOCO DE HASH BCRYPT \_ \_ \_**
</dt> <dd> <dl> <dt>

L"HashBlockLength"
</dt> <dt>



O tamanho, em bytes, do bloco para um hash. Essa propriedade só se aplica a algoritmos de hash. Esse tipo de dados é **um DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**COMPRIMENTO DE HASH BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"HashDigestLength"
</dt> <dt>



O tamanho, em bytes, do valor de hash de um provedor de hash. Esse tipo de dados é **um DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**BCRYPT \_ HASH \_ OID \_ LIST**
</dt> <dd> <dl> <dt>

L"HashOIDList"
</dt> <dt>



A lista de [*identificadores*](/windows/desktop/SecGloss/d-gly)de objeto de hash codificados por DER [](/windows/desktop/SecGloss/o-gly) (OIDs). Essa propriedade é uma [**estrutura \_ OID \_ LIST BCRYPT.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) Essa propriedade só pode ser lida.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**VETOR DE INICIALIZAÇÃO BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"IV"
</dt> <dt>



Contém o [*IV (vetor de inicialização)*](/windows/desktop/SecGloss/i-gly) de uma chave. Essa propriedade se aplica somente a chaves.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**COMPRIMENTO DA CHAVE BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"KeyLength"
</dt> <dt>



O tamanho, em bits, do valor de chave de um provedor de chave simétrica. Esse tipo de dados é **um DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**COMPRIMENTOS \_ DE CHAVE BCRYPT \_**
</dt> <dd> <dl> <dt>

L"KeyLengths"
</dt> <dt>



Os comprimentos de chave com suporte pelo algoritmo. Essa propriedade é uma [**estrutura \_ \_ \_ STRUCT BCRYPT KEY LENGTHS.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) Essa propriedade se aplica somente a algoritmos.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**BCRYPT \_ KEY \_ OBJECT \_ LENGTH**
</dt> <dd> <dl> <dt>

L"KeyObjectLength"
</dt> <dt>



Essa propriedade não é usada. A **propriedade BCRYPT \_ OBJECT \_ LENGTH** é usada para obter essas informações.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**BCRYPT \_ KEY \_ STRENGTH**
</dt> <dd> <dl> <dt>

L"KeyStrength"
</dt> <dt>



O número de bits na chave. Esse tipo de dados é **um DWORD.** Essa propriedade se aplica somente a chaves.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**COMPRIMENTO DO \_ BLOCO \_ DE MENSAGEM \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"MessageBlockLength"
</dt> <dt>



Isso pode ser definido em qualquer alça de chave que tenha o modo de encadeamento CFB definido. Por padrão, essa propriedade é definida como 1 para CFB de 8 bits. Defini-lo para o tamanho do bloco em bytes faz com que o CFB de bloco completo seja usado. Para chaves XTS, ele é usado para definir o tamanho, em bytes, da Unidade de Dados XTS (normalmente 512 ou 4096).


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT \_ MULTI \_ OBJECT \_ LENGTH**
</dt> <dd> <dl> <dt>

L"MultiObjectLength"
</dt> <dt>



Essa propriedade retorna um [**\_ \_ \_ \_ STRUCT BCRYPT MULTI OBJECT LENGTH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), que contém as informações necessárias para calcular o tamanho de um buffer de objeto. Essa propriedade só tem suporte em versões do sistema operacional que suportam a [**função BCryptCreateMultiHash.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash)


</dt> </dl> </dd> <dt>

<span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**COMPRIMENTO DO OBJETO BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"ObjectLength"
</dt> <dt>



O tamanho, em bytes, do subobjeto de um provedor. Esse tipo de dados é **um DWORD.** Atualmente, os provedores de algoritmo de criptografia simétrica e hash usam buffers alocados pelo chamador para armazenar seus subobjetos. Por exemplo, o provedor de hash exige que você aloce memória para o objeto de hash obtido com a [**função BCryptCreateHash.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) Essa propriedade fornece o tamanho do buffer para o objeto de um provedor para que você possa alocar memória para o objeto criado pelo provedor.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**ESQUEMAS \_ DE PREENCHIMENTO BCRYPT \_**
</dt> <dd> <dl> <dt>

L"PaddingSchemes"
</dt> <dt>



Representa o esquema de preenchimento do provedor de algoritmo RSA. Esse tipo de dados é **um DWORD.** Esse pode ser um dos valores a seguir.



| Identificador                             | Valor      | Descrição                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| **ROTEADOR DE PAINEL COM SUPORTE DE BCRYPT \_ \_ \_**     | 0x00000001 | O provedor dá suporte ao preenchimento adicionado pelo roteador.         |
| **BCRYPT \_ SUPPORTED \_ PAD \_ PKCS1 \_ ENC** | 0x00000002 | O provedor dá suporte ao esquema de preenchimento de criptografia PKCS1. |
| **BCRYPT \_ SUPPORTED \_ PAD \_ PKCS1 \_ SIG** | 0x00000004 | O provedor dá suporte ao esquema de preenchimento de assinatura PKCS1.  |
| **BCRYPT \_ SUPPORTED \_ PAD \_ OAEP**       | 0x00000008 | O provedor dá suporte ao esquema de preenchimento OAEP.             |
| **BCRYPT \_ SUPPORTED \_ PAD \_ PSS**        | 0x00000010 | O provedor dá suporte ao esquema de preenchimento PSS.              |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**BCRYPT \_ PROVIDER \_ HANDLE**
</dt> <dd> <dl> <dt>

L"ProviderHandle"
</dt> <dt>



O identificador do provedor CNG que criou o objeto passado no *parâmetro hObject.* Esse tipo de dados é um **IDENTIFICADOr \_ ALG \_ BCRYPT.** Essa propriedade só pode ser recuperada; ele não pode ser definido.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**COMPRIMENTO DA ASSINATURA BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"SignatureLength"
</dt> <dt>



O tamanho, em bytes, do comprimento de uma assinatura para uma chave. Esse tipo de dados é **um DWORD.** Essa propriedade se aplica somente a chaves. Essa propriedade só pode ser recuperada; ele não pode ser definido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Bcrypt.h</dt> </dl> |



 

