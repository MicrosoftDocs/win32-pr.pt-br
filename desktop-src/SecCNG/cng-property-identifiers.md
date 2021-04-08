---
description: Usado com as funções BCryptGetProperty e BCryptSetProperty para identificar uma propriedade.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Identificadores de propriedade primitiva de criptografia (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f4996a216fbc4fbf63216f99b5f630c4769e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826815"
---
# <a name="cryptography-primitive-property-identifiers"></a>Identificadores de propriedade primitiva de criptografia

Os valores a seguir são usados com as funções [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) e [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) para identificar uma propriedade.

<dl> <dt>

<span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**\_nome do algoritmo BCRYPT \_**
</dt> <dd> <dl> <dt>

L "algorithmName"
</dt> <dt>



Uma cadeia de caracteres Unicode terminada em nulo que contém o nome do algoritmo.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**\_comprimento da \_ marca de autenticação BCRYPT \_**
</dt> <dd> <dl> <dt>

L "AuthTagLength"
</dt> <dt>



Os comprimentos de marca de autenticação que são suportados pelo algoritmo. Essa propriedade é uma estrutura de struct de comprimento de uma [**\_ marca de autenticação \_ \_ \_ BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) . Essa propriedade só se aplica a algoritmos.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**\_tamanho do bloco BCRYPT \_**
</dt> <dd> <dl> <dt>

L "BlockLength"
</dt> <dt>



O tamanho, em bytes, de um bloco de codificação para o algoritmo. Essa propriedade só se aplica a algoritmos de codificação de bloco. Esse tipo de dados é um **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**\_lista de \_ tamanho de bloco BCRYPT \_**
</dt> <dd> <dl> <dt>

L "BlockSizelist"
</dt> <dt>



Uma lista de comprimentos de bloco com suporte por um algoritmo de criptografia. Esse tipo de dados é uma matriz de **DWORDs**. O número de elementos na matriz pode ser determinado pela divisão do número de bytes recuperados pelo tamanho de uma única **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**\_modo de ENCADEAMENTO \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "ChainingMode"
</dt> <dt>



Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que representa o modo de encadeamento do algoritmo de criptografia. Essa propriedade pode ser definida em um identificador de algoritmo ou um identificador de chave para um dos valores a seguir.



| Identificador                   | Valor                         | Descrição                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_CBC do \_ modo de cadeia BCRYPT \_** | L "ChainingModeCBC"<br/> | Define o modo de encadeamento do algoritmo para [*encadeamento de blocos de codificação*](/windows/desktop/SecGloss/c-gly).<br/>            |
| **\_CCM de \_ modo de cadeia BCRYPT \_** | L "ChainingModeCCM"<br/> | Define o modo de encadeamento do algoritmo como Counter com o modo CBC-MAC (CCM). **Windows Vista:** Esse valor tem suporte a partir do Windows Vista com SP1.<br/> <br/> |
| **\_modo de cadeia BCRYPT \_ \_ CFB** | L "ChainingModeCFB"<br/> | Define o modo de encadeamento do algoritmo como [*comentários de codificação*](/windows/desktop/SecGloss/c-gly).<br/>                              |
| **\_ \_ ECB modo de cadeia de BCRYPT \_** | L "ChainingModeECB"<br/> | Define o modo de encadeamento do algoritmo como [*Electronic Codebook*](/windows/desktop/SecGloss/e-gly).<br/>                  |
| **\_modo de cadeia BCRYPT \_ \_ GCM** | L "ChainingModeGCM"<br/> | Define o modo de encadeamento do algoritmo para o modo Galois/Counter (GCM). **Windows Vista:** Esse valor tem suporte a partir do Windows Vista com SP1.<br/> <br/>       |
| **\_modo de cadeia BCRYPT \_ \_ na**  | L "ChainingModeN/A"<br/> | O algoritmo não dá suporte ao encadeamento.<br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**parâmetros da BCRYPT \_ DH \_**
</dt> <dd> <dl> <dt>

L "DHParameters"
</dt> <dt>



Especifica os parâmetros a serem usados com uma chave de Diffie-Hellman. Esse tipo de dados é um ponteiro para uma estrutura de [**\_ cabeçalho de \_ parâmetro \_ BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) . Essa propriedade só pode ser definida e deve ser definida para a chave antes de a chave ser concluída.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**\_parâmetros de DSA de BCRYPT \_**
</dt> <dd> <dl> <dt>

L "DSAParameters"
</dt> <dt>



Especifica os parâmetros a serem usados com uma chave DSA. Esta propriedade é um [**\_ cabeçalho de \_ parâmetro \_ BCrypt DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) ou uma estrutura de cabeçalho de parâmetro de [**BCrypt \_ DSA \_ \_ \_ v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) . Essa propriedade só pode ser definida e deve ser definida para a chave antes de a chave ser concluída.

**Windows 8:** A partir do Windows 8, essa propriedade pode ser uma estrutura [**v2 de cabeçalho de parâmetro de BCRYPT \_ DSA \_ \_ \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) . Use esta estrutura se o tamanho da chave exceder 1024 bits e for menor ou igual a 3072 bits. Se o tamanho da chave for maior ou igual a 512, mas menor ou igual a 1024 bits, use a estrutura de [**\_ cabeçalho do \_ parâmetro \_ BCRYPT DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**tamanho de chave de BCRYPT \_ efetivo \_ \_**
</dt> <dd> <dl> <dt>

L "EffectiveKeyLength"
</dt> <dt>



O tamanho, em bits, do comprimento efetivo de uma chave RC2. Esse tipo de dados é um **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**\_tamanho do \_ bloco de hash BCRYPT \_**
</dt> <dd> <dl> <dt>

L "HashBlockLength"
</dt> <dt>



O tamanho, em bytes, do bloco para um hash. Essa propriedade se aplica somente a algoritmos de hash. Esse tipo de dados é um **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**\_tamanho do hash BCRYPT \_**
</dt> <dd> <dl> <dt>

L "HashDigestLength"
</dt> <dt>



O tamanho, em bytes, do valor de hash de um provedor de hash. Esse tipo de dados é um **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**\_lista de \_ OID de hash BCRYPT \_**
</dt> <dd> <dl> <dt>

L "HashOIDList"
</dt> <dt>



A lista de OIDs ( [*identificadores de objeto*](/windows/desktop/SecGloss/o-gly) hash) codificados em [*der*](/windows/desktop/SecGloss/d-gly). Essa propriedade é uma estrutura de [**\_ \_ lista de OID BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) . Esta propriedade só pode ser lida.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**\_vetor de inicialização de BCRYPT \_**
</dt> <dd> <dl> <dt>

L "IV"
</dt> <dt>



Contém o [*vetor de inicialização*](/windows/desktop/SecGloss/i-gly) (IV) para uma chave. Essa propriedade só se aplica a chaves.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**\_comprimento da chave BCRYPT \_**
</dt> <dd> <dl> <dt>

L "KeyLength"
</dt> <dt>



O tamanho, em bits, do valor de chave de um provedor de chave simétrica. Esse tipo de dados é um **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**\_comprimentos de chave BCRYPT \_**
</dt> <dd> <dl> <dt>

L "keycomprimentos"
</dt> <dt>



Os comprimentos de chave que são suportados pelo algoritmo. Essa propriedade é uma estrutura de [**\_ struct de \_ tamanho \_ de chave BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) . Essa propriedade só se aplica a algoritmos.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**\_comprimento do \_ objeto de chave BCRYPT \_**
</dt> <dd> <dl> <dt>

L "KeyObjectLength"
</dt> <dt>



Essa propriedade não é usada. A propriedade de **\_ \_ comprimento do objeto BCRYPT** é usada para obter essas informações.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**\_restrição de chave BCRYPT \_**
</dt> <dd> <dl> <dt>

L "keyforça"
</dt> <dt>



O número de bits na chave. Esse tipo de dados é um **DWORD**. Essa propriedade só se aplica a chaves.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**\_comprimento do \_ bloco de mensagens BCRYPT \_**
</dt> <dd> <dl> <dt>

L "MessageBlockLength"
</dt> <dt>



Isso pode ser definido em qualquer identificador de chave que tenha o modo de encadeamento de CFB definido. Por padrão, essa propriedade é definida como 1 para CFB de 8 bits. Configurá-lo para o tamanho do bloco em bytes faz com que o CFB de bloco completo seja usado. Para chaves XTS, ela é usada para definir o tamanho, em bytes, da unidade de dados XTS (geralmente 512 ou 4096).


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**\_tamanho de vários \_ objetos \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "MultiObjectLength"
</dt> <dt>



Essa propriedade retorna um [**\_ struct de \_ \_ comprimento \_ de vários objetos BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), que contém as informações necessárias para calcular o tamanho de um buffer de objeto. Essa propriedade só tem suporte em versões de sistema operacional que dão suporte à função [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**\_tamanho do objeto BCRYPT \_**
</dt> <dd> <dl> <dt>

L "ObjectLength"
</dt> <dt>



O tamanho, em bytes, do subobjeto de um provedor. Esse tipo de dados é um **DWORD**. Atualmente, os provedores de hash e de algoritmo de criptografia simétrica usam buffers alocados pelo chamador para armazenar seus subobjetos. Por exemplo, o provedor de hash exige que você aloque memória para o objeto de hash obtido com a função [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) . Essa propriedade fornece o tamanho do buffer para o objeto de um provedor para que você possa alocar memória para o objeto criado pelo provedor.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**\_esquemas de preenchimento BCRYPT \_**
</dt> <dd> <dl> <dt>

L "PaddingSchemes"
</dt> <dt>



Representa o esquema de preenchimento do provedor de algoritmo RSA. Esse tipo de dados é um **DWORD**. Isso pode ser um dos valores a seguir.



| Identificador                             | Valor      | Descrição                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| **\_roteador de \_ teclado com suporte em BCRYPT \_**     | 0x00000001 | O provedor dá suporte ao preenchimento adicionado pelo roteador.         |
| **BCRYPT \_ com suporte do \_ pad \_ PKCS1 \_ ENC** | 0x00000002 | O provedor dá suporte ao esquema de preenchimento de criptografia PKCS1. |
| **BCRYPT \_ com suporte do \_ pad \_ PKCS1 \_ SIG** | 0x00000004 | O provedor dá suporte ao esquema de preenchimento de assinatura PKCS1.  |
| **BCRYPT \_ \_ OAEP pad com suporte \_**       | 0x00000008 | O provedor dá suporte ao esquema de preenchimento OAEP.             |
| **\_teclado compatível com BCRYPT \_ \_ PSS**        | 0x00000010 | O provedor oferece suporte ao esquema de preenchimento PSS.              |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**\_identificador do provedor BCRYPT \_**
</dt> <dd> <dl> <dt>

L "ProviderHandle"
</dt> <dt>



O identificador do provedor CNG que criou o objeto passado no parâmetro *hObject* . Esse tipo de dados é **um \_ \_ identificador BCRYPT alg**. Esta propriedade só pode ser recuperada; Ele não pode ser definido.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**\_tamanho da assinatura BCRYPT \_**
</dt> <dd> <dl> <dt>

L "SignatureLength"
</dt> <dt>



O tamanho, em bytes, do comprimento de uma assinatura para uma chave. Esse tipo de dados é um **DWORD**. Essa propriedade só se aplica a chaves. Esta propriedade só pode ser recuperada; Ele não pode ser definido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Bcrypt. h</dt> </dl> |



 

