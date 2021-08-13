---
description: Permite que um aplicativo de transporte consulte o pacote de segurança do Credential Security Support Provider (CredSSP) para determinados atributos de um contexto de segurança.
ms.assetid: 4956c4ab-b71e-4960-b750-f3a79b87baac
title: Função QueryContextAttributes (CredSSP) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b8ff421a2173f2ce2c5521e0706b53c3f6c326038179345d139acd0a157c7d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920225"
---
# <a name="querycontextattributes-credssp-function"></a>Função QueryContextAttributes (CredSSP)

A função **QueryContextAttributes (CredSSP)** permite que um aplicativo de transporte consulte o pacote de segurança do Credential Security Support Provider (CredSSP) para determinados [*atributos*](../secgloss/a-gly.md#_security_attribute_gly) de um contexto de segurança.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS SEC_ENTRY QueryContextAttributes(
  _In_  PCtxtHandle phContext,
  _In_  ULONG       ulAttribute,
  _Out_ PVOID       pBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phContext* \[ no\]
</dt> <dd>

Um identificador para o contexto de segurança a ser consultado.

</dd> <dt>

*ulAttribute* \[ no\]
</dt> <dd>

O atributo do contexto a ser retornado. Esse parâmetro pode usar um dos valores a seguir. A menos que especificado de outra forma, os atributos são aplicáveis ao cliente e ao servidor.



| Valor                                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_C_ACCESS_TOKEN"></span><span id="secpkg_attr_c_access_token"></span><dl> <dt>**SECPKG \_ 0x80000012 \_ de \_ \_ token de acesso C attr**</dt> <dt></dt> </dl>                                 | O parâmetro *pBuffer* contém um ponteiro para uma estrutura [**SecPkgContext \_ AccessToken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) que especifica o token de acesso para o contexto de segurança atual.<br/> Esse atributo tem suporte apenas no servidor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_C_FULL_ACCESS_TOKEN"></span><span id="secpkg_attr_c_full_access_token"></span><dl> <dt>**SECPKG \_ 0x80000082 \_ do \_ \_ \_ token de acesso completo do attr C**</dt> <dt></dt> </dl>                 | O parâmetro *pBuffer* contém um ponteiro para uma estrutura [**SecPkgContext \_ AccessToken**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) que especifica o token de acesso para o contexto de segurança atual.<br/> Esse atributo tem suporte apenas no servidor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_ATTR_CERT_TRUST_STATUS"></span><span id="secpkg_attr_cert_trust_status"></span><dl> <dt>**SECPKG \_ 0x80000084 \_ de \_ \_ status de confiança de certificado attr**</dt> <dt></dt> </dl>                        | O parâmetro *pBuffer* contém um ponteiro para uma estrutura de [**\_ \_ status de confiança de certificado**](/windows/win32/api/wincrypt/ns-wincrypt-cert_trust_status) que especifica informações de confiança sobre o certificado.<br/> Esse atributo tem suporte apenas no cliente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_CREDS"></span><span id="secpkg_attr_creds"></span><dl> <dt>**SECPKG \_ ATTR \_ creds**</dt> <dt>0x80000080</dt> </dl>                                                              | O parâmetro *pBuffer* contém um ponteiro para uma estrutura [**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) que especifica as credenciais do cliente.<br/> As credenciais do cliente podem ser nome de usuário e senha ou nome de usuário e PIN de cartão inteligente.<br/> Esse atributo tem suporte apenas no servidor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ ATTR \_ creds \_ 2**</dt> <dt>0x80000086</dt> </dl>                                                       | O parâmetro *pBuffer* contém um ponteiro para uma estrutura [**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) que especifica as credenciais do cliente. <br/> Se a credencial do cliente for o nome de usuário e a senha, o buffer será uma estrutura de [**\_ \_ logon interativo KERB**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) em pacote.<br/> Se a credencial do cliente for nome de usuário e PIN de cartão inteligente, o buffer será uma estrutura de [**\_ \_ logon de certificado KERB**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) empacotada.<br/> Se a credencial do cliente for uma credencial de identidade online, o buffer será uma estrutura [**\_ EX2 de \_ identidade de autenticação \_ \_ WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) de marshaling.<br/> Esse atributo tem suporte apenas no servidor CredSSP.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/> |
| <span id="SECPKG_ATTR_NEGOTIATION_PACKAGE"></span><span id="secpkg_attr_negotiation_package"></span><dl> <dt>**SECPKG \_ 0x80000081 \_ do \_ pacote de negociação attr**</dt> <dt></dt> </dl>                   | O parâmetro *pBuffer* contém um ponteiro para uma estrutura [**SecPkgContext \_ PackageInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) que especifica o nome do pacote de autenticação negociado pelo provedor [Microsoft Negotiate](microsoft-negotiate.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informações do pacote attr**</dt> <dt>10</dt> </dl>                                                | O parâmetro *pBuffer* contém um ponteiro para uma [**estrutura \_ PackageInfo SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkginfoa).<br/> Retorna informações sobre o SSP em uso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_SERVER_AUTH_FLAGS"></span><span id="secpkg_attr_server_auth_flags"></span><dl> <dt>**SECPKG \_ \_Sinalizadores de \_ autenticação \_ de servidor attr**</dt> <dt>0x80000083</dt> </dl>                        | O parâmetro *pBuffer* contém um ponteiro para uma estrutura de [**\_ sinalizadores SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) que especifica informações sobre os sinalizadores no contexto de segurança atual.<br/> Esse atributo tem suporte apenas no cliente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ \_Tamanhos de attr**</dt> <dt>0x0</dt> </dl>                                                                     | O parâmetro *pBuffer* contém um ponteiro para uma estrutura de [**\_ tamanhos de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .<br/> Consulta os tamanhos das estruturas usadas nas trocas de autenticação e funções por mensagem.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="SECPKG_ATTR_SUBJECT_SECURITY_ATTRIBUTES"></span><span id="secpkg_attr_subject_security_attributes"></span><dl> <dt>**SECPKG \_ \_Atributos de \_ segurança \_ da entidade attr**</dt> <dt>124</dt> </dl> | O parâmetro *pBuffer* contém um ponteiro para uma [**estrutura \_ subjectattributes do SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_subjectattributes) .<br/> Esse valor retorna informações sobre os atributos de segurança para a conexão.<br/> Esse valor só tem suporte no servidor CredSSP.<br/> **Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pBuffer* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura que recebe os atributos. O tipo de estrutura depende do valor do parâmetro *ulAttribute* .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem sucedido, retornará s \_ E \_ OK.

Se a função falhar, ela poderá retornar os códigos de erro a seguir.



| Código/valor de retorno                                                                                                                                                            | Descrição                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E \_ \_ identificador inválido**</dt> <dt>0x80100003</dt> </dl>       | A função falhou. O parâmetro *phContext* especifica um identificador para um contexto incompleto.<br/> |
| <dl> <dt>**S \_ E \_ \_ função sem suporte**</dt> <dt>0X80090302</dt> </dl> | A função falhou. O valor do parâmetro *ulAttribute* não é válido.<br/>                 |



 

## <a name="remarks"></a>Comentários

A estrutura apontada pelo parâmetro *pBuffer* varia dependendo do atributo que está sendo consultado.

Embora o chamador deva alocar a estrutura *pBuffer* em si, o SSP aloca qualquer memória necessária para manter membros de tamanho variável da estrutura *pBuffer* . A memória alocada pelo SSP deve ser liberada chamando a função [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nomes Unicode e ANSI<br/>   | **QueryContextAttributesW** (Unicode) e **QueryContextAttributesA** (ANSI)<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**contexto do certificado \_**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds)
</dt> <dt>

[**Tamanhos de SecPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> </dl>

 

 
