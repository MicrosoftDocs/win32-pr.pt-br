---
description: Permite que um aplicativo de transporte consulte o [*pacote de segurança*](../secgloss/s-gly.md) de resumo para determinados atributos de um [*contexto de segurança*](../secgloss/s-gly.md).
ms.assetid: d4cd2cc4-77a2-42ba-9029-f4d92706c5c2
title: Função QueryContextAttributes (Digest) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 11cf8cbd35242b43d3f68b6265daae02e1d5425a8c0692742cbee0a1bd93441d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920205"
---
# <a name="querycontextattributes-digest-function"></a>Função QueryContextAttributes (Digest)

A função **QueryContextAttributes (Digest)** permite que um aplicativo de transporte consulte o [*pacote de segurança*](../secgloss/s-gly.md) Digest para determinados [*atributos*](../secgloss/a-gly.md#_security_attribute_gly) de um [*contexto de segurança*](../secgloss/s-gly.md).

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

Um identificador para o [*contexto de segurança*](../secgloss/s-gly.md) a ser consultado.

</dd> <dt>

*ulAttribute* \[ no\]
</dt> <dd>

Especifica o atributo do contexto a ser retornado. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_ATTR_ACCESS_TOKEN"></span><span id="secpkg_attr_access_token"></span><dl> <dt>**SECPKG \_ \_ \_ Token de acesso attr**</dt> <dt>18</dt> </dl>                                   | O parâmetro *pBuffer* contém um ponteiro para uma [**estrutura \_ AccessToken SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_accesstoken) .<br/> Retorna um identificador para o token de acesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_AUTHORITY"></span><span id="secpkg_attr_authority"></span><dl> <dt>**SECPKG \_ \_Autoridade attr**</dt> <dt>6</dt> </dl>                                              | O parâmetro *pBuffer* contém um ponteiro para uma estrutura de [**\_ autoridade SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya) .<br/> Consulta o nome da autoridade de autenticação.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="SECPKG_ATTR_CLIENT_SPECIFIED_TARGET"></span><span id="secpkg_attr_client_specified_target"></span><dl> <dt>**SECPKG \_ O \_ cliente attr \_ especificou o \_ destino**</dt> <dt>27</dt> </dl> | O parâmetro *pBuffer* contém um ponteiro para uma estrutura [**SecPkgContext \_ CLIENTSPECIFIEDTARGET**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_clientspecifiedtarget) que representa o SPN (nome da entidade de serviço) do destino inicial fornecido pelo cliente. <br/> Esse valor tem suporte apenas ao usar associações de canal.<br/> **Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_CREDS_2"></span><span id="secpkg_attr_creds_2"></span><dl> <dt>**SECPKG \_ ATTR \_ creds \_ 2**</dt> <dt>0x80000086</dt> </dl>                                          | O parâmetro *pBuffer* contém um ponteiro para uma estrutura [**SecPkgContext \_ ClientCreds**](/windows/win32/api/credssp/ns-credssp-secpkgcontext_clientcreds) que especifica as credenciais do cliente. <br/> Se a credencial do cliente for o nome de usuário e a senha, o buffer será uma estrutura de [**\_ \_ logon interativo KERB**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_interactive_logon) em pacote.<br/> Se a credencial do cliente for nome de usuário e PIN de cartão inteligente, o buffer será uma estrutura de [**\_ \_ logon de certificado KERB**](/windows/win32/api/ntsecapi/ns-ntsecapi-kerb_certificate_logon) empacotada.<br/> Se a credencial do cliente for uma credencial de identidade online, o buffer será uma estrutura [**\_ EX2 de \_ identidade de autenticação \_ \_ WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) de marshaling.<br/> Esse atributo tem suporte apenas no servidor CredSSP.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/> |
| <span id="SECPKG_ATTR_DCE_INFO"></span><span id="secpkg_attr_dce_info"></span><dl> <dt>**SECPKG \_ ATTR \_ \_ informações de DCE**</dt> <dt>3</dt> </dl>                                                | O parâmetro *pBuffer* contém um ponteiro para uma [**estrutura \_ DceInfo SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo) .<br/> Consultas de dados de autorização usados pelos serviços de DCE.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_FLAGS"></span><span id="secpkg_attr_flags"></span><dl> <dt>**SECPKG \_ \_Sinalizadores de attr**</dt> <dt>14</dt> </dl>                                                         | O parâmetro *pBuffer* contém um ponteiro para uma estrutura de [**\_ sinalizadores SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_flags) .<br/> Retorna informações sobre os sinalizadores de contexto negociados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="SECPKG_ATTR_KEY_INFO"></span><span id="secpkg_attr_key_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informações da chave attr**</dt> <dt>5</dt> </dl>                                                | O parâmetro *pBuffer* contém um ponteiro para uma estrutura de [**\_ KeyInfo SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa) .<br/> Consulta informações sobre as chaves usadas em um [*contexto de segurança*](../secgloss/s-gly.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SECPKG_ATTR_LIFESPAN"></span><span id="secpkg_attr_lifespan"></span><dl> <dt>**SECPKG \_ \_Ciclo de vida de attr**</dt> <dt>2</dt> </dl>                                                 | O parâmetro *pBuffer* contém um ponteiro para uma estrutura de [**\_ vida útil SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan) .<br/> Consulta o período de vida do contexto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_LOCAL_CRED"></span><span id="secpkg_attr_local_cred"></span><dl> <dt>**SECPKG \_ attr \_ local \_ cred**</dt> </dl>                                                                                                 | O parâmetro *pBuffer* contém um ponteiro para uma **estrutura \_ LocalCredentialInfo SecPkgContext** . (obsoleto)<br/> Substituído pelo contexto de \_ \_ certificado local SECPKG attr \_ \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="SECPKG_ATTR_NAMES"></span><span id="secpkg_attr_names"></span><dl> <dt>**SECPKG \_ \_Nomes de attr**</dt> <dt>1</dt> </dl>                                                          | O parâmetro *pBuffer* contém um ponteiro para uma estrutura de [**\_ nomes de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa) .<br/> Consulta o nome associado ao contexto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="SECPKG_ATTR_NATIVE_NAMES"></span><span id="secpkg_attr_native_names"></span><dl> <dt>**SECPKG \_ \_ \_ Nomes nativos de attr**</dt> <dt>13</dt> </dl>                                   | O parâmetro *pBuffer* contém um ponteiro para uma [**estrutura \_ nativa de SecPkgContext**](https://docs.microsoft.com/windows/win32/api/sspi/ns-sspi-_secpkgcontext_nativenamesa) .<br/> Retorna o nome da entidade de segurança (CNAME) do tíquete de saída.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="SECPKG_ATTR_NEGOTIATION_INFO"></span><span id="secpkg_attr_negotiation_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informações de negociação de attr**</dt> <dt>12</dt> </dl>                       | O parâmetro *pBuffer* contém um ponteiro para uma [**estrutura \_ NegotiationInfo SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_negotiationinfoa) .<br/> Retorna informações sobre o [*pacote de segurança*](../secgloss/s-gly.md) a ser usado com o processo de negociação e o estado atual da negociação para o uso desse pacote.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_ATTR_PACKAGE_INFO"></span><span id="secpkg_attr_package_info"></span><dl> <dt>**SECPKG \_ \_ \_ Informações do pacote attr**</dt> <dt>10</dt> </dl>                                   | O parâmetro *pBuffer* contém um ponteiro para uma [**estrutura \_ PackageInfo SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .<br/> Retorna informações sobre o SSP em uso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_PASSWORD_EXPIRY"></span><span id="secpkg_attr_password_expiry"></span><dl> <dt>**SECPKG \_ Atributo \_ de \_ expiração de senha de attr**</dt> <dt>8</dt> </dl>                           | O parâmetro *pBuffer* contém um ponteiro para uma [**estrutura \_ PasswordExpiry SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_passwordexpiry) .<br/> Retorna informações de expiração de senha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SECPKG_ATTR_ROOT_STORE"></span><span id="secpkg_attr_root_store"></span><dl> <dt>**SECPKG \_ 0x55 \_ de \_ armazenamento raiz attr**</dt> <dt></dt> </dl>                                       | O parâmetro *pBuffer* contém um ponteiro para um **HCERTCONTEXT**. Localiza um contexto de certificado que contém um certificado fornecido pelo repositório raiz.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="SECPKG_ATTR_SESSION_KEY"></span><span id="secpkg_attr_session_key"></span><dl> <dt>**SECPKG \_ \_ \_ Chave de sessão attr**</dt> <dt>9</dt> </dl>                                       | O parâmetro *pBuffer* contém um ponteiro para uma [**estrutura \_ SessionKey SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sessionkey) .<br/> Retorna informações sobre a [*chave de sessão*](../secgloss/s-gly.md)s.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SECPKG_ATTR_SIZES"></span><span id="secpkg_attr_sizes"></span><dl> <dt>**SECPKG \_ \_Tamanhos de attr**</dt> <dt>0</dt> </dl>                                                          | O parâmetro *pBuffer* contém um ponteiro para uma estrutura de [**\_ tamanhos de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .<br/> Consulta os tamanhos das estruturas usadas nas funções por mensagem.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_ATTR_STREAM_SIZES"></span><span id="secpkg_attr_stream_sizes"></span><dl> <dt>**SECPKG \_ \_ \_ Tamanhos de fluxo de attr**</dt> <dt>4</dt> </dl>                                    | O parâmetro *pBuffer* contém um ponteiro para uma [**estrutura \_ StreamSizes SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) .<br/> Consulta os tamanhos das várias partes de um fluxo usado nas funções por mensagem.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="SECPKG_ATTR_TARGET_INFORMATION"></span><span id="secpkg_attr_target_information"></span><dl> <dt>**SECPKG \_ \_ \_ Informações de destino de attr**</dt> <dt>17</dt> </dl>                 | O parâmetro *pBuffer* contém um ponteiro para uma [**estrutura \_ TargetInformation SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_targetinformation) .<br/> Retorna informações sobre o nome do servidor remoto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pBuffer* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura que recebe os atributos. O tipo de estrutura apontada depende do valor especificado no parâmetro *ulAttribute* .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será s \_ E \_ OK.

Se a função falhar, o valor de retorno será um código de erro diferente de zero.

## <a name="remarks"></a>Comentários

A estrutura apontada pelo parâmetro *pBuffer* varia dependendo do atributo que está sendo consultado. O chamador deve alocar a estrutura *pBuffer* em si, mas o SSP aloca qualquer memória necessária para manter membros de tamanho variável da estrutura *pBuffer* . A memória alocada pelo SSP pode ser liberada chamando a função [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Depois que o \_ \_ contexto de certificado remoto attr SECPKG ou o valor do contexto de \_ \_ \_ certificado local SECPKG attr \_ \_ \_ tiver sido lido, o membro **HCERTSTORE** será definido como um identificador para um repositório de certificados que contenha os certificados intermediários, se houver. Além disso, o aplicativo é responsável por chamar [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) para liberar a memória usada pelo contexto do certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                   |
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

[**\_Autoridade SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_authoritya)
</dt> <dt>

[**SecPkgContext \_ ConnectionInfo**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_connectioninfo)
</dt> <dt>

[**SecPkgContext \_ DceInfo**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_dceinfo)
</dt> <dt>

[**SecPkgContext \_ IssuerListInfoEx**](/windows/win32/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)
</dt> <dt>

[**KeyInfo de SecPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_keyinfoa)
</dt> <dt>

[**\_Vida útil do SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_lifespan)
</dt> <dt>

[**Nomes de SecPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_namesa)
</dt> <dt>

[**Tamanhos de SecPkgContext \_**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes)
</dt> <dt>

[**SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes)
</dt> </dl>

 

 
