---
description: As constantes a seguir são usadas pela API de proteção de dados CNG.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: Constantes CNG DPAPI (NCryptprotect. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457267"
---
# <a name="cng-dpapi-constants"></a>Constantes CNG DPAPI

As constantes a seguir são usadas pela API de proteção de dados CNG.

<dl> <dt>

<span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**\_ \_ delimitador de decrescente \_ de NCRYPT e**
</dt> <dd> <dl> <dt>

L "E"
</dt> <dt>



Pode ser usado para testar uma cadeia de caracteres de descritor de proteção para um delimitador AND.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**é \_ igual a decrescente de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "="
</dt> <dt>



Pode ser usado para testar uma cadeia de caracteres de descritor de proteção para um sinal de igual.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**\_ \_ delimitador de decrescente \_ de NCRYPT ou**
</dt> <dd> <dl> <dt>

L "OU"
</dt> <dt>



Pode ser usado para testar uma cadeia de caracteres de descritor de proteção para um delimitador ou.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**\_algoritmo de proteção de chave NCRYPT \_ \_ \_ local**
</dt> <dd> <dl> <dt>

"LOCAL"
</dt> <dt>



O descritor de proteção LOCAL protege o conteúdo para a sessão de logon, o usuário atual ou o computador local, conforme identificado pelas seguintes constantes:

-   **\_ \_ logon local de proteção de chave NCRYPT \_ \_**
-   **\_ \_ usuário local de proteção de chave NCRYPT \_ \_**
-   **\_ \_ máquina local de proteção de chave NCRYPT \_ \_**


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**\_SDDL de \_ algoritmo de proteção de chave NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

SDDL
</dt> <dt>



Protege o conteúdo a uma cadeia de caracteres SDDL (linguagem de definição de descritor de segurança) que contém informações de descritor de segurança.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**\_SID do \_ algoritmo de proteção de chave NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

SIDs
</dt> <dt>



O descritor de proteção SID contém um grupo ou uma identidade principal.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**\_WEBcredentials do algoritmo de proteção de chave NCRYPT \_ \_ \_**
</dt> <dd> <dl> <dt>

"Webcredentials"
</dt> <dt>



Protege as credenciais da conta da Web de um usuário.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**\_ \_ logon local de proteção de chave NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

logon
</dt> <dt>



Protege o conteúdo à sessão de logon atual. Os usuários não poderão descriptografar o conteúdo protegido após o logoff ou a reinicialização.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**\_ \_ máquina local de proteção de chave NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

Tradução
</dt> <dt>



Protege o conteúdo para o computador local. Todos os usuários no computador local podem descriptografar o conteúdo protegido.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**\_ \_ usuário local de proteção de chave NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

usuário
</dt> <dt>



Protege o conteúdo à sessão atual do usuário. Somente esse usuário no computador local poderá descriptografar o conteúdo protegido.


</dt> </dl> </dd> <dt>

<span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**\_provedor de \_ proteção de chave MS \_**
</dt> <dd> <dl> <dt>

"Provedor de proteção de chave da Microsoft"
</dt> <dt>



Representa o provedor de proteção de chave da Microsoft que dá suporte a formatos representados pelas seguintes constantes:

-   **\_SID do \_ algoritmo de proteção de chave NCRYPT \_ \_**
-   **\_algoritmo de proteção de chave NCRYPT \_ \_ \_ local**
-   **\_SDDL de \_ algoritmo de proteção de chave NCRYPT \_ \_**


</dt> </dl> </dd> <dt>

<span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**\_provedor de \_ proteção de chave do cliente do Windows \_ \_**
</dt> <dd> <dl> <dt>

"Provedor de proteção de chave do cliente do Windows"
</dt> <dt>



Representa o provedor de proteção de chave da Microsoft que está disponível somente no cliente e que oferece suporte a formatos representados pelas seguintes constantes:

-   **\_WEBcredentials do algoritmo de proteção de chave NCRYPT \_ \_ \_**


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>NCryptprotect. h</dt> </dl> |



 

 




