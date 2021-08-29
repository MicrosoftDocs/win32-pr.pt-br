---
title: Constantes de HTTP_AUTH_ENABLE_ (http. h)
description: Defina os esquemas de autenticação que podem ser habilitados em um grupo de URLs.
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa66013700dc1ad6b091ccf4738f2af456cb29384fd2d48b2d17a0a244019a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394494"
---
# <a name="http_auth_enable_-constants"></a>\_Constantes http auth \_ Enable \_

As constantes **http \_ auth \_ Enable** definem os esquemas de autenticação que podem ser habilitados em um grupo de URLs.

Essas constantes são usadas na estrutura [**de \_ \_ \_ informações de autenticação do servidor http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) .

<dl> <dt>

<span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**\_habilitação de http auth \_ \_ básico**
</dt> <dd> <dl> <dt>



O esquema de autenticação básica está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP \_ auth \_ Enable \_ Digest**
</dt> <dd> <dl> <dt>



O esquema de autenticação Digest está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP \_ auth \_ habilitar \_ Kerberos**
</dt> <dd> <dl> <dt>



O esquema de autenticação Kerberos está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**\_sinalizador http auth \_ ex habilitar o cache de \_ \_ \_ \_ credenciais Kerberos \_**
</dt> <dd> <dl> <dt>



O cache de credenciais Kerberos está habilitado.

**Windows Server 2003 e anteriores:** Não disponível.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**\_ \_ \_ \_ credencial de captura de sinalizador http auth ex \_**
</dt> <dd> <dl> <dt>



A API do servidor HTTP captura a identidade do chamador e a usa para autenticação somente para esquemas Negotiate e Kerberos.

**Windows Server 2003 e anteriores:** Não disponível.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP \_ auth \_ habilitar \_ NTLM**
</dt> <dd> <dl> <dt>



O esquema de autenticação NTLM está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**\_ \_ habilitar \_ negociação de http auth**
</dt> <dd> <dl> <dt>



O esquema de autenticação Negotiate está habilitado.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**\_ \_ habilitar \_ todos os http auth**
</dt> <dd> <dl> <dt>



Todos os esquemas de autenticação estão habilitados.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes da API do servidor HTTP versão 2,0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_informações de \_ autenticação do servidor http \_**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





