---
description: Usado para identificar uma propriedade de armazenamento de chaves.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Identificadores de Armazenamento chave (Ncrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b8fca27591837a555e4f75040ba16056c42e16ce488c0bb99f2d8f7de70bd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907607"
---
# <a name="key-storage-property-identifiers"></a>Identificadores de Armazenamento chave

Os valores a seguir são usados para identificar uma propriedade de armazenamento de chaves.

<dl> <dt>

<span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**PROPRIEDADE DE GRUPO \_ DE ALGORITMOS NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"Algorithm Group"
</dt> <dt>



Uma cadeia de caracteres Unicode terminada em nulo que contém o nome do grupo de algoritmos do objeto. Essa propriedade se aplica somente a chaves. Os identificadores a seguir são retornados pelo provedor de armazenamento de chaves da Microsoft.



| Identificador                                     | Valor              | Descrição                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| **NCRYPT \_ RSA \_ ALGORITHM \_ GROUP**<br/>   | "RSA"<br/>   | O grupo de algoritmos RSA.<br/>                           |
| **NCRYPT \_ DH \_ ALGORITHM \_ GROUP**<br/>    | "DH"<br/>    | O grupo Diffie-Hellman algoritmo.<br/>                |
| **GRUPO DE \_ ALGORITMOS NCRYPT DSA \_ \_**<br/>   | "DSA"<br/>   | O grupo de algoritmos DSA.<br/>                           |
| **NCRYPT \_ ECDSA \_ ALGORITHM \_ GROUP**<br/> | "ECDSA"<br/> | O grupo de algoritmos DSA de curva elíptica.<br/>            |
| **NCRYPT \_ ECDH \_ ALGORITHM \_ GROUP**<br/>  | "ECDH"<br/>  | A curva elíptica Diffie-Hellman grupo de algoritmos.<br/> |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**PROPRIEDADE DE ALGORITMO NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"Nome do Algoritmo"
</dt> <dt>



Uma cadeia de caracteres Unicode terminada em nulo que contém o nome do algoritmo do objeto. Pode ser um dos Identificadores de Algoritmo [**CNG**](cng-algorithm-identifiers.md) predefinidos ou outro identificador de algoritmo registrado. Essa propriedade se aplica somente a chaves.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**NCRYPT \_ ASSOCIATED \_ ECDH \_ KEY**
</dt> <dd> <dl> <dt>

L"SmartCardAssociatedECDHKey"
</dt> <dt>



Um **valor LPWSTR** que indica o nome do contêiner da chave ECDH (Curva Elíptica Diffie-Hellman) a ser usada durante o logon para um determinado handle para uma chave ECDSA (Algoritmo de Assinatura Digital de Curva Elíptica). Se não houver chaves ECDH no cartão, o KSP (provedor de [*armazenamento*](/windows/desktop/SecGloss/k-gly) de chaves) retornará **NTE \_ NOT \_ FOUND.** Essa propriedade se aplica às chaves ECDSA para logon com cartões inteligentes. A propriedade é suportada pelo provedor de armazenamento de chaves do Cartão Inteligente da Microsoft e não pelo provedor de armazenamento de chaves de Software da Microsoft.

**Windows Server 2008 e Windows Vista:** Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**PROPRIEDADE COMPRIMENTO \_ DO \_ BLOCO NCRYPT \_**
</dt> <dd> <dl> <dt>

L"Comprimento do Bloco"
</dt> <dt>



Uma **DWORD** que contém o comprimento, em bytes, do bloco de criptografia. Essa propriedade se aplica somente a chaves que suportam criptografia.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**PROPRIEDADE NCRYPT \_ CERTIFICATE \_**
</dt> <dd> <dl> <dt>

L"SmartCardKeyCertificate"
</dt> <dt>



Um [*BLOB*](/windows/desktop/SecGloss/b-gly) que contém um certificado X.509 associado à chave.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Um [*BLOB que*](/windows/desktop/SecGloss/b-gly) contém o [*certificado de chave de*](/windows/desktop/SecGloss/s-gly) cartão [*inteligente*](/windows/desktop/SecGloss/c-gly). Essa propriedade não é suportada pelo provedor microsoft software key Armazenamento.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**PROPRIEDADE \_ NCRYPT DH \_ PARAMETERS \_**
</dt> <dd> <dl> <dt>

L"DHParameters"
</dt> <dt>



Especifica parâmetros a ser usado com uma Diffie-Hellman chave. Esse tipo de dados é um ponteiro para uma estrutura [**\_ BCRYPT DH \_ PARAMETER \_ HEADER.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Essa propriedade só pode ser definida e deve ser definida para a chave antes que a chave seja concluída.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**PROPRIEDADE NCRYPT \_ EXPORT \_ POLICY \_**
</dt> <dd> <dl> <dt>

L"Exportar Política"
</dt> <dt>



Uma **DWORD** que contém um conjunto de sinalizadores que especificam a política de exportação para uma chave persistente. Essa propriedade se aplica somente a chaves. Isso pode conter zero ou uma combinação de um ou mais dos valores a seguir.



| Identificador                                    | Valor      | Descrição                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NCRYPT \_ ALLOW \_ EXPORT \_ FLAG**               | 0x00000001 | A chave privada pode ser exportada.                                                                                                                                                                                                                                                                                 |
| **NCRYPT \_ ALLOW \_ PLAINTEXT \_ EXPORT \_ FLAG**    | 0x00000002 | A chave privada pode ser exportada em formato de texto não criptografado.                                                                                                                                                                                                                                                               |
| **SINALIZADOR NCRYPT \_ \_ ALLOW \_ ARCHIVING**            | 0x00000004 | A chave privada pode ser exportada uma vez para fins de arquivamento. Esse sinalizador só se aplica ao alça de chave original no qual ele está definido. Essa política só pode ser aplicada ao alça de chave original. Depois que o alça de chave tiver sido fechado, a chave não poderá mais ser exportada para fins de arquivamento.                   |
| **NCRYPT \_ ALLOW \_ PLAINTEXT \_ ARCHIVING \_ FLAG** | 0x00000008 | A chave privada pode ser exportada uma vez em formato de texto não criptografado para fins de arquivamento. Esse sinalizador só se aplica ao alça de chave original no qual ele está definido. Essa política só pode ser aplicada ao alça de chave original. Depois que o alça de chave tiver sido fechado, a chave não poderá mais ser exportada para fins de arquivamento. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**PROPRIEDADE DE \_ TIPO NCRYPT IMPL \_ \_**
</dt> <dd> <dl> <dt>

L"Tipo Impl"
</dt> <dt>



Um **DWORD** que contém um conjunto de sinalizadores que definem os detalhes de implementação do provedor. Essa propriedade se aplica somente a provedores de armazenamento de chaves. Isso pode conter zero ou uma combinação de um ou mais dos valores a seguir.



| Identificador                            | Valor      | Descrição                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| **SINALIZADOR DE \_ HARDWARE NCRYPT IMPL \_ \_**      | 0x00000001 | O provedor é baseado em hardware.                           |
| **SINALIZADOR DE \_ SOFTWARE NCRYPT IMPL \_ \_**      | 0x00000002 | O provedor é baseado em software.                           |
| **SINALIZADOR \_ REMOVÍVEL NCRYPT IMPL \_ \_**     | 0x00000008 | O provedor é removível.                                |
| **SINALIZADOR NCRYPT \_ IMPL \_ HARDWARE \_ RNG \_** | 0x00000010 | O provedor é um gerador de número aleatório baseado em hardware. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**PROPRIEDADE NCRYPT \_ KEY \_ TYPE \_**
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



Indica se o provedor dá suporte a descritores de segurança para chaves. Essa propriedade é uma **DWORD** que contém 1 se o provedor oferece suporte a descritores de segurança para chaves. Se essa propriedade contiver qualquer outro valor ou se a função [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) retornar **NTE \_ NOT \_ SUPPORTED**, o provedor não dá suporte a descritores de segurança para chaves. Essa propriedade se aplica somente a provedores.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**PROPRIEDADE GUID \_ DE CARTÃO INTELIGENTE NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"SmartCardGuid"
</dt> <dt>



Um BLOB que contém o identificador do cartão inteligente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**PROPRIEDADE NCRYPT \_ UI \_ \_ POLICY**
</dt> <dd> <dl> <dt>

L"UI Policy"
</dt> <dt>



Se usado com a [**função NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) ou [**NCryptGetProperty,**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) esse é um ponteiro para uma estrutura [**NCRYPT \_ UI \_ POLICY**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) que contém a política de interface do usuário de chave forte para a chave. Essa propriedade se aplica somente a chaves persistentes. Essa propriedade só pode ser definida quando a chave está sendo gerada. Depois que [**a função NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) tiver sido chamada para essa chave, essa propriedade se tornará somente leitura.

Um provedor de armazenamento de chaves pode receber esse parâmetro por meio de uma função de retorno de chamada [**NCryptSetPropertyFn.**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) O valor do parâmetro é uma estrutura NCRYPT \_ UI \_ POLICY \_ BLOB que contém as mesmas informações. Da mesma forma, quando um aplicativo faz uma solicitação por meio de NCryptSetPropertyFn para o provedor retornar essa propriedade, espera-se que o provedor retorne uma estrutura NCRYPT \_ UI \_ POLICY \_ BLOB.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**PROPRIEDADE NCRYPT \_ UNIQUE \_ \_ NAME**
</dt> <dd> <dl> <dt>

L"Unique Name"
</dt> <dt>



Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o nome exclusivo do objeto. Esse é um nome alternativo que pode ser usado ao acessar a chave. Essa propriedade é usada quando se pensa que o nome da chave originalmente passado para [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) não é exclusivo o suficiente para identificar de forma confiável a chave persistente. O provedor de armazenamento de chaves da Microsoft retornará o nome do arquivo da chave como esta propriedade.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**PROPRIEDADE DE CONTEXTO NCRYPT \_ \_ \_ USE**
</dt> <dd> <dl> <dt>

L"Usar Contexto"
</dt> <dt>



Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que descreve o contexto da operação. Essa propriedade não é persistente e pode ser definida em um provedor ou em uma chave. Uma chave não tem acesso à propriedade **NCRYPT \_ USE CONTEXT \_ \_ PROPERTY** do provedor porque a propriedade é específica apenas para o handle para o qual está definida.

Um exemplo em que essa propriedade seria usada no contexto de um provedor é um provedor de armazenamento de chaves que precisa solicitar ao usuário durante uma chamada para [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (por exemplo, "Inserir seu cartão inteligente no leitor."). Como o alça de chave não está disponível até que **NCryptOpenKey** retorne, o aplicativo deve definir essa propriedade no handle do provedor antes de chamar **NCryptOpenKey**.

Um exemplo em que essa propriedade seria usada no contexto de um guidão de chave é um provedor de armazenamento de chaves que precisa solicitar ao usuário durante uma operação usando a chave (por exemplo, "Este aplicativo precisa usar essa chave para assinar um documento."). O provedor pode retransmitir essas informações de contexto para o usuário em qualquer interface do usuário mostrada durante a operação.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**PROPRIEDADE NCRYPT \_ USE \_ COUNT \_ \_ ENABLED**
</dt> <dd> <dl> <dt>

L"Enabled Use Count"
</dt> <dt>



Indica se o provedor dá suporte à contagem de uso para chaves. Essa propriedade é uma **DWORD que** contém 1 se o provedor dá suporte à contagem de uso para chaves. Se essa propriedade contiver qualquer outro valor ou se a função [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) retornar **NTE \_ NOT \_ SUPPORTED**, o provedor não dá suporte à contagem de uso para chaves. Essa propriedade se aplica somente a provedores.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**PROPRIEDADE NCRYPT \_ USE \_ \_ COUNT**
</dt> <dd> <dl> <dt>

L"Use Count"
</dt> <dt>



Uma [**variável \_ INTEGER ULARGE**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) que contém o número de operações que a chave [*privada especificada*](/windows/desktop/SecGloss/p-gly) realizou. Essa propriedade é opcional e pode não ter suporte de todos os provedores. Os provedores que suportam essa propriedade em chaves também devem dar suporte à propriedade **NCRYPT \_ USE COUNT \_ \_ ENABLED \_ PROPERTY** no alça do provedor. O provedor de armazenamento de chaves da Microsoft não dá suporte a essa propriedade. Essa propriedade se aplica somente a chaves persistentes.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**PROPRIEDADE NCRYPT \_ USER \_ \_ CERTSTORE**
</dt> <dd> <dl> <dt>

L"SmartCardUserCertStore"
</dt> <dt>



Um **HCERTSTORE que** representa o repositório de certificados de usuário do cartão inteligente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**PROPRIEDADE DE \_ VERSÃO NCRYPT \_**
</dt> <dd> <dl> <dt>

L"Version"
</dt> <dt>



Um **DWORD** que contém a versão de software do provedor. A palavra alta contém a versão principal e a palavra baixa contém a versão secundária. Por exemplo, 0x00030033 = 3,51. Essa propriedade se aplica somente a provedores.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**PROPRIEDADE NCRYPT \_ WINDOW \_ HANDLE \_**
</dt> <dd> <dl> <dt>

L"HWND Handle"
</dt> <dt>



Um ponteiro para o **HWND**(alça de janela) a ser usado como o pai de qualquer interface do usuário exibida.

Como um comportamento indesejável pode acontecer quando uma interface do usuário é mostrada usando um alça de janela **NULL** para o pai, é recomendável que um provedor de armazenamento de chaves não exibir uma interface do usuário, a menos que essa propriedade esteja definida.


</dt> </dl> </dd> </dl>

Os valores a seguir são usados para definir limites de dados de propriedade.



| Constante/valor                                                                                                                                                                                                                                                 | Descrição                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <dt>**NCRYPT \_ DADOS \_ DE PROPRIEDADE MAX \_ 0X100000**</dt> <dt></dt> </dl> | Especifica o tamanho máximo de um valor da propriedade, em bytes.<br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <dt>**NCRYPT \_ MAX \_ PROPERTY \_ NAME**</dt> <dt>64</dt> </dl>       | Especifica o tamanho máximo de um nome de propriedade, em caracteres.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Ncrypt.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

