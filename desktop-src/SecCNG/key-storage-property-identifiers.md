---
description: Usado para identificar uma propriedade de armazenamento de chave.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Identificadores de propriedade de armazenamento de chave (NCrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 813a15ba106989cb558eba181bc893d75c6d1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783246"
---
# <a name="key-storage-property-identifiers"></a>Identificadores de propriedade de armazenamento de chave

Os valores a seguir são usados para identificar uma propriedade de armazenamento de chave.

<dl> <dt>

<span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**\_Propriedade do grupo de algoritmos NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "grupo de algoritmos"
</dt> <dt>



Uma cadeia de caracteres Unicode terminada em nulo que contém o nome do grupo de algoritmos do objeto. Essa propriedade só se aplica a chaves. Os identificadores a seguir são retornados pelo provedor de armazenamento de chaves da Microsoft.



| Identificador                                     | Valor              | Descrição                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| **\_grupo de \_ algoritmos do RSA NCRYPT \_**<br/>   | RSA<br/>   | O grupo de algoritmos RSA.<br/>                           |
| **\_grupo de \_ algoritmos DH NCRYPT \_**<br/>    | FEITA<br/>    | O grupo de algoritmos Diffie-Hellman.<br/>                |
| **\_grupo de \_ algoritmos DSA NCRYPT \_**<br/>   | DSA<br/>   | O grupo de algoritmos DSA.<br/>                           |
| **\_grupo de \_ algoritmos de ECDSA NCRYPT \_**<br/> | ECDSA<br/> | O grupo de algoritmos DSA de curva elíptica.<br/>            |
| **\_grupo de \_ algoritmos de ECDH NCRYPT \_**<br/>  | ECDH<br/>  | O grupo de algoritmos Diffie-Hellman de curva elíptica.<br/> |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**\_propriedade de algoritmo NCRYPT \_**
</dt> <dd> <dl> <dt>

L "nome do algoritmo"
</dt> <dt>



Uma cadeia de caracteres Unicode terminada em nulo que contém o nome do algoritmo do objeto. Pode ser um dos [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) predefinidos ou outro identificador de algoritmo registrado. Essa propriedade só se aplica a chaves.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**\_ \_ chave ECDH associada de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardAssociatedECDHKey"
</dt> <dt>



Um valor de **LPWSTR** que indica o nome do contêiner da chave de Diffie-Hellman de curva elíptica (ECDH) a ser usada durante o logon de um determinado identificador para uma chave de ECDSA (algoritmo de assinatura digital de curva elíptica). Se não houver nenhuma chave ECDH no cartão, o KSP ( [*provedor de armazenamento de chaves*](/windows/desktop/SecGloss/k-gly) ) retornará o **nte \_ não \_ encontrado**. Essa propriedade se aplica a chaves ECDSA para logon com cartões inteligentes. A propriedade é suportada pelo provedor de armazenamento de chaves de cartão inteligente da Microsoft e não pelo provedor de armazenamento de chaves de software da Microsoft.

**Windows Server 2008 e Windows Vista:** Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**\_propriedade de \_ comprimento de bloco NCRYPT \_**
</dt> <dd> <dl> <dt>

L "comprimento do bloco"
</dt> <dt>



Um **DWORD** que contém o comprimento, em bytes, do bloco de criptografia. Essa propriedade só se aplica a chaves que dão suporte à criptografia.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**\_propriedade de certificado NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardKeyCertificate"
</dt> <dt>



Um [*blob*](/windows/desktop/SecGloss/b-gly) que contém um certificado X. 509 que está associado à chave.

**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Um [*blob*](/windows/desktop/SecGloss/b-gly) que contém o [*certificado*](/windows/desktop/SecGloss/c-gly)de chave do [*cartão inteligente*](/windows/desktop/SecGloss/s-gly) . Não há suporte para essa propriedade no provedor de armazenamento de chaves de software da Microsoft.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**Propriedade NCRYPT de \_ \_ parâmetros DH \_**
</dt> <dd> <dl> <dt>

L "DHParameters"
</dt> <dt>



Especifica os parâmetros a serem usados com uma chave de Diffie-Hellman. Esse tipo de dados é um ponteiro para uma estrutura de [**\_ cabeçalho de \_ parâmetro \_ BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) . Essa propriedade só pode ser definida e deve ser definida para a chave antes de a chave ser concluída.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**\_propriedade de \_ política de exportação NCRYPT \_**
</dt> <dd> <dl> <dt>

L "exportar política"
</dt> <dt>



Um **DWORD** que contém um conjunto de sinalizadores que especificam a política de exportação para uma chave persistente. Essa propriedade só se aplica a chaves. Isso pode conter zero ou uma combinação de um ou mais dos valores a seguir.



| Identificador                                    | Valor      | Descrição                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NCRYPT \_ permitir \_ sinalizador de exportação \_**               | 0x00000001 | A chave privada pode ser exportada.                                                                                                                                                                                                                                                                                 |
| **NCRYPT \_ permitir \_ \_ sinalizador de exportação de texto não criptografado \_**    | 0x00000002 | A chave privada pode ser exportada em formato de texto sem formatação.                                                                                                                                                                                                                                                               |
| **NCRYPT \_ permitir \_ sinalizador de arquivamento \_**            | 0x00000004 | A chave privada pode ser exportada uma vez para fins de arquivamento. Esse sinalizador se aplica somente ao identificador de chave original no qual ele está definido. Essa política só pode ser aplicada ao identificador de chave original. Depois que o identificador de chave for fechado, a chave não poderá mais ser exportada para fins de arquivamento.                   |
| **NCRYPT \_ permitir \_ \_ sinalizador de arquivamento de texto não criptografado \_** | 0x00000008 | A chave privada pode ser exportada uma vez em formato de texto sem formatação para fins de arquivamento. Esse sinalizador se aplica somente ao identificador de chave original no qual ele está definido. Essa política só pode ser aplicada ao identificador de chave original. Depois que o identificador de chave for fechado, a chave não poderá mais ser exportada para fins de arquivamento. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**\_Propriedade do \_ tipo NCRYPT impl \_**
</dt> <dd> <dl> <dt>

L "tipo de impl"
</dt> <dt>



Um **DWORD** que contém um conjunto de sinalizadores que definem os detalhes de implementação do provedor. Essa propriedade só se aplica a provedores de armazenamento de chaves. Isso pode conter zero ou uma combinação de um ou mais dos valores a seguir.



| Identificador                            | Valor      | Descrição                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| **\_sinalizador de \_ hardware NCRYPT impl \_**      | 0x00000001 | O provedor é baseado em hardware.                           |
| **\_sinalizador de \_ software NCRYPT impl \_**      | 0x00000002 | O provedor é baseado em software.                           |
| **sinalizador de removível de NCRYPT \_ impl \_ \_**     | 0x00000008 | O provedor é removível.                                |
| **\_sinalizador de \_ RNG de hardware NCRYPT impl \_ \_** | 0x00000010 | O provedor é um gerador de números aleatórios com base em hardware. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**\_propriedade de \_ tipo de chave NCRYPT \_**
</dt> <dd> <dl> <dt>

L "tipo de chave"
</dt> <dt>



Um **DWORD** que contém um conjunto de sinalizadores que definem o tipo de chave. Essa propriedade só se aplica a chaves. Isso pode conter zero ou o valor a seguir.



| Identificador                     | Valor      | Descrição                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| **\_sinalizador de \_ chave de máquina NCRYPT \_** | 0x00000001 | A chave se aplica ao computador local. Se esse sinalizador não estiver presente, a chave se aplicará ao usuário atual. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**\_propriedade de \_ uso de chave NCRYPT \_**
</dt> <dd> <dl> <dt>

L "uso da chave"
</dt> <dt>



Um **DWORD** que contém um conjunto de sinalizadores que definem os detalhes de uso de uma chave. Essa propriedade só se aplica a chaves. Isso pode conter zero ou uma combinação de um ou mais dos valores a seguir.



| Identificador                              | Valor      | Descrição                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| **NCRYPT \_ permitir \_ sinalizador de descriptografia \_**        | 0x00000001 | A chave pode ser usada para descriptografia.                  |
| **NCRYPT \_ permitir \_ sinalizador de assinatura \_**        | 0x00000002 | A chave pode ser usada para assinatura.                     |
| **NCRYPT \_ permitir \_ \_ sinalizador de contrato de chave \_** | 0x00000004 | A chave pode ser usada para criptografia de contrato secreto. |
| **NCRYPT \_ permitir \_ todos os \_ usos**          | 0x00ffffff | A chave pode ser usada para qualquer finalidade.                 |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**\_Propriedade NCRYPT última \_ modificação \_**
</dt> <dd> <dl> <dt>

L "Modified"
</dt> <dt>



Indica quando a chave foi modificada pela última vez. Esse tipo de dados é um ponteiro para uma estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) . Essa propriedade só se aplica a chaves persistentes.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**\_propriedade de comprimento NCRYPT \_**
</dt> <dd> <dl> <dt>

L "comprimento"
</dt> <dt>



Um **DWORD** que contém o comprimento, em bits, da chave. Essa propriedade só se aplica a chaves.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**\_propriedade de comprimentos NCRYPT \_**
</dt> <dd> <dl> <dt>

L "comprimentos"
</dt> <dt>



Indica os tamanhos de chave que são suportados pela chave. Esse tipo de dados é um ponteiro para uma estrutura de [**\_ \_ comprimentos com suporte NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) que contém essas informações. Essa propriedade só se aplica a chaves.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**\_propriedade de \_ comprimento de nome Max \_ NCRYPT \_**
</dt> <dd> <dl> <dt>

L "comprimento máximo do nome"
</dt> <dt>



Um **DWORD** que contém o comprimento máximo, em caracteres, do nome de uma chave persistente. Essa propriedade se aplica somente a um provedor.

Essa propriedade destina-se principalmente a ser usada por provedores de armazenamento de chaves que armazenam suas chaves em um dispositivo que tem uma quantidade limitada de memória disponível, como um cartão inteligente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**\_propriedade de nome NCRYPT \_**
</dt> <dd> <dl> <dt>

L "nome"
</dt> <dt>



Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome do objeto.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**\_propriedade de \_ prompt de PIN NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardPinPrompt"
</dt> <dt>



Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**\_propriedade de PIN NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardPin"
</dt> <dt>



Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o PIN. O PIN é usado para uma chave de cartão inteligente ou a senha para uma chave protegida por senha armazenada em um KSP baseado em software. Esta propriedade só pode ser definida. O Microsoft KSPs armazenará esse valor em cache para que o usuário seja solicitado apenas uma vez por processo.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**\_propriedade de \_ identificador do provedor NCRYPT \_**
</dt> <dd> <dl> <dt>

L "identificador do provedor"
</dt> <dt>



Um **\_ \_ identificador de Prov de NCRYPT** que contém o identificador do provedor de armazenamento de chaves CNG. Quando terminar de usar o identificador, você deverá chamar [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) para liberá-lo.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**\_propriedade de leitor NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardReader"
</dt> <dt>



Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome do leitor de cartão inteligente. Esta propriedade só pode ser definida.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**\_ \_ Propriedade CERTSTORE de raiz NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartcardRootCertStore"
</dt> <dt>



Um **HCERTSTORE** que representa o repositório de certificados raiz do cartão inteligente.


</dt> </dl> </dd> <dt>

<span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_ \_ \_ ID do PIN do scartar**
</dt> <dd> <dl> <dt>

L "SmartCardPinId"
</dt> <dt>



Um ponteiro para o valor da **\_ ID de PIN** associado a uma determinada [*chave de criptografia*](/windows/desktop/SecGloss/c-gly) em um [*cartão inteligente*](/windows/desktop/SecGloss/s-gly). Trata-se de uma propriedade somente leitura. O tipo de dados **\_ ID do PIN** é definido em cardmod. h.

**Windows Server 2008 e Windows Vista:** Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**informações de PIN de NCRYPT \_ scartar \_ \_**
</dt> <dd> <dl> <dt>

L "SmartCardPinInfo"
</dt> <dt>



Um ponteiro para [**fixar \_**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) a estrutura de informações do PIN associado a uma determinada chave de criptografia no cartão inteligente. O chamador fornece o identificador de chave. Esta propriedade é uma propriedade somente leitura. A estrutura de **\_ informações de PIN** é definida em cardmod. h.

**Windows Server 2008 e Windows Vista:** Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**\_Propriedade NCRYPT Secure \_ PIN \_**
</dt> <dd> <dl> <dt>

L "SmartCardSecurePin"
</dt> <dt>



Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o PIN da sessão de cartão inteligente. Esta propriedade só pode ser definida.

**Windows Vista:** Não há suporte para essa propriedade.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**\_propriedade de \_ Descrição de segurança de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "Descrição de segurança"
</dt> <dt>



Um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que contém informações de controle de acesso para a chave. Essa propriedade só se aplica a chaves persistentes. O parâmetro *dwFlags* da função [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) ou [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) identifica a parte do descritor de segurança a ser obtido ou definido.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**\_propriedade de \_ suporte do descr de segurança NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "suporte a descr de segurança"
</dt> <dt>



Indica se o provedor dá suporte a descritores de segurança para chaves. Essa propriedade é uma **DWORD** que contém 1 se o provedor oferece suporte a descritores de segurança para chaves. Se essa propriedade contiver qualquer outro valor, ou se a função [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) retornar o **nte \_ sem \_ suporte**, o provedor não oferecerá suporte a descritores de segurança para chaves. Essa propriedade só se aplica a provedores.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**\_propriedade de GUID de cartão inteligente NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "SmartCardGuid"
</dt> <dt>



Um BLOB que contém o identificador do cartão inteligente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**\_propriedade de \_ política de IU NCRYPT \_**
</dt> <dd> <dl> <dt>

L "diretiva de interface do usuário"
</dt> <dt>



Se usado com a função [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) ou [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) , esse é um ponteiro para uma estrutura de [**\_ \_ diretiva de interface do usuário NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) que contém a diretiva de interface de usuários de chave forte para a chave. Essa propriedade só se aplica a chaves persistentes. Essa propriedade só pode ser definida quando a chave está sendo gerada. Depois que a função [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) tiver sido chamada para essa chave, essa propriedade se tornará somente leitura.

Um provedor de armazenamento de chaves pode receber esse parâmetro por meio de uma função de retorno de chamada [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) . O valor do parâmetro é uma \_ estrutura de blob de diretiva de interface do usuário NCRYPT \_ \_ que contém as mesmas informações. Da mesma forma, quando um aplicativo faz uma solicitação por meio de NCryptSetPropertyFn ao provedor para retornar essa propriedade, espera-se que o provedor retorne uma \_ estrutura de blob de política de interface do usuário NCRYPT \_ \_ .


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**\_propriedade de \_ nome \_ exclusivo NCRYPT**
</dt> <dd> <dl> <dt>

L "nome exclusivo"
</dt> <dt>



Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome exclusivo do objeto. Esse é um nome alternativo que pode ser usado ao acessar a chave. Essa propriedade é usada quando é pensado que o nome da chave originalmente passado para [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) não é exclusivo o suficiente para identificar de forma confiável a chave persistente. O provedor de armazenamento de chaves da Microsoft retornará o nome do arquivo da chave como essa propriedade.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT \_ \_ propriedade de contexto de uso \_**
</dt> <dd> <dl> <dt>

L "usar contexto"
</dt> <dt>



Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que descreve o contexto da operação. Essa propriedade não é persistente e pode ser definida em um provedor ou em uma chave. Uma chave não tem acesso à propriedade de **\_ propriedade de \_ contexto \_ de uso NCRYPT** do provedor porque a propriedade é específica somente para o identificador para o qual ela está definida.

Um exemplo em que essa propriedade seria usada no contexto de um provedor é um provedor de armazenamento de chaves que precisa solicitar ao usuário durante uma chamada para [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (por exemplo, "Insira seu cartão inteligente no leitor."). Como o identificador de chave não está disponível até que **NCryptOpenKey** seja retornado, o aplicativo deve definir essa propriedade no identificador do provedor antes de chamar **NCryptOpenKey**.

Um exemplo em que essa propriedade seria usada no contexto de um identificador de chave é um provedor de armazenamento de chaves que precisa solicitar ao usuário durante uma operação usando a chave (por exemplo, "este aplicativo precisa usar essa chave para assinar um documento."). Em seguida, o provedor poderia retransmitir essas informações de contexto para o usuário em qualquer interface do usuário mostrada durante a operação.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**\_propriedade de uso de \_ contagem \_ HABILITAda de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "contagem de uso habilitada"
</dt> <dt>



Indica se o provedor dá suporte à contagem de uso para chaves. Essa propriedade é uma **DWORD** que contém 1 se o provedor oferece suporte à contagem de uso para chaves. Se essa propriedade contiver qualquer outro valor, ou se a função [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) retornar o **nte \_ sem \_ suporte**, o provedor não oferecerá suporte à contagem de uso para chaves. Essa propriedade só se aplica a provedores.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**\_propriedade de \_ contagem de uso NCRYPT \_**
</dt> <dd> <dl> <dt>

L "contagem de uso"
</dt> <dt>



Uma variável de [**\_ inteiro ULARGE**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) que contém o número de operações que a [*chave privada*](/windows/desktop/SecGloss/p-gly) especificada executou. Essa propriedade é opcional e pode não ter suporte de todos os provedores. Os provedores que oferecem suporte a essa propriedade nas chaves também devem oferecer suporte à propriedade de **\_ propriedade de uso \_ \_ habilitado \_ da contagem de utilização de NCRYPT** no identificador do provedor. O provedor de armazenamento de chaves da Microsoft não oferece suporte a essa propriedade. Essa propriedade só se aplica a chaves persistentes.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**\_ \_ Propriedade CERTSTORE de usuário NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardUserCertStore"
</dt> <dt>



Um **HCERTSTORE** que representa o repositório de certificados do usuário do cartão inteligente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**\_propriedade de versão NCRYPT \_**
</dt> <dd> <dl> <dt>

L "versão"
</dt> <dt>



Um **DWORD** que contém a versão de software do provedor. A palavra alta contém a versão principal e a palavra inferior contém a versão secundária. Por exemplo, 0x00030033 = 3,51. Essa propriedade só se aplica a provedores.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**\_propriedade de \_ identificador de janela NCRYPT \_**
</dt> <dd> <dl> <dt>

L "identificador HWND"
</dt> <dt>



Um ponteiro para o identificador de janela (**HWND**) a ser usado como o pai de qualquer interface do usuário que é exibida.

Como um comportamento indesejável pode ocorrer quando uma interface do usuário é mostrada usando um identificador de janela **nulo** para o pai, é altamente recomendável que um provedor de armazenamento de chaves não exiba uma interface do usuário, a menos que essa propriedade esteja definida.


</dt> </dl> </dd> </dl>

Os valores a seguir são usados para definir limites de dados de propriedade.



| Constante/valor                                                                                                                                                                                                                                                 | Descrição                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <dt>**NCRYPT \_ 0x100000 \_ de \_ dados de propriedade Max**</dt> <dt></dt> </dl> | Especifica o tamanho máximo de um valor de propriedade, em bytes.<br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <dt>**NCRYPT \_ \_ \_ Nome de propriedade máx**</dt> . <dt>64</dt> </dl>       | Especifica o tamanho máximo de um nome de propriedade, em caracteres.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>NCrypt. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

