---
title: Atributo User-Account-Control
description: Sinalizadores que controlam o comportamento da conta de usuário.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo User-Account-Control
- Esquema do AD do atributo userAccountControl
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76ab64d0d93ce7523c3d91d6f4a3ebb5f4d200f0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468793"
---
# <a name="user-account-control-attribute"></a>Atributo User-Account-Control

Sinalizadores que controlam o comportamento da conta de usuário.



| Entrada | Valor |
|-------------------|---------------------------------------|
| CN                | Controle de conta de usuário                  |
| Ldap-Display-Name | userAccountControl                    |
| Tamanho              | 4 bytes.                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.      |
| Frequência de atualização  | Cada vez que a política de conta é muda. |
| Attribute-Id      | 1.2.840.113556.1.4.8                  |
| System-Id-Guid    | bf967a68-0de6-11d0-a285-00aa003049e2  |
| Sintaxe            | [**Enumeração**](s-enumeration.md)  |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No Catálogo Global      | Verdadeiro                              |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No Catálogo Global      | Verdadeiro                              |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No Catálogo Global      | Verdadeiro                              |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No Catálogo Global      | Verdadeiro                              |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No Catálogo Global      | Verdadeiro                              |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No Catálogo Global      | Verdadeiro                              |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="remarks"></a>Comentários

Esse valor de atributo pode ser zero ou uma combinação de um ou mais dos valores a seguir.




| Valor hexadecimal | Identificador (definido em iads.h) | Descrição | 
|-------------------|--------------------------------|-------------|
| 0x00000001 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a> | O script de logon é executado. | 
| 0x00000002 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a> | A conta de usuário está desabilitada. | 
| 0x00000008 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a> | O diretório home é necessário. | 
| 0x00000010 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a> | No momento, a conta está bloqueada. | 
| 0x00000020 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a> | Nenhuma senha é necessária. | 
| 0x00000040 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a> | O usuário não pode alterar a senha.<blockquote>[!Note]<br />Não é possível atribuir as configurações de permissão PASSWD_CANT_CHANGE modificando diretamente o atributo UserAccountControl. Para obter mais informações e um exemplo de código que mostra como impedir que um usuário altere a senha, consulte <a href="/windows/desktop/ADSI/user-cannot-change-password">User Cannot Change Password</a>.</blockquote><br /> : | 
| 0x00000080 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a> | O usuário pode enviar uma senha criptografada. | 
| 0x00000100 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a> | Essa é uma conta para usuários cuja conta primária está em outro domínio. Essa conta fornece acesso de usuário a esse domínio, mas não a nenhum domínio que confie nesse domínio. Também conhecida como uma conta de usuário local. | 
| 0x00000200 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a> | Esse é um tipo de conta padrão que representa um usuário típico. | 
| 0x00000800 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a> | Essa é uma permissão para confiar na conta de um domínio do sistema que confia em outros domínios. | 
| 0x00001000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a> | Essa é uma conta de computador para um computador que é membro desse domínio. | 
| 0x00002000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a> | Essa é uma conta de computador para um controlador de domínio de backup do sistema que é membro desse domínio. | 
| 0x00004000 | N/D | Não usado. | 
| 0x00008000 | N/D | Não usado. | 
| 0x00010000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a> | A senha dessa conta nunca expirará. | 
| 0x00020000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a> | Essa é uma conta de logon do MNS. | 
| 0x00040000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a> | O usuário deve fazer logoff usando um cartão inteligente. | 
| 0x00080000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a> | A conta de serviço (conta de usuário ou computador), na qual um serviço é executado, é confiável para a delegação kerberos. Qualquer serviço desse tipo pode representar um cliente solicitando o serviço. | 
| 0x00100000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a> | O contexto de segurança do usuário não será delegado a um serviço, mesmo que a conta de serviço seja definida como confiável para delegação kerberos. | 
| 0x00200000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a> | Restrinja essa entidade de segurança a usar somente tipos de criptografia DES (Data Encryption Standard) para chaves. | 
| 0x00400000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a> | Essa conta não exige a pré-autenticação Kerberos para logon. | 
| 0x00800000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a> | A senha do usuário expirou. Esse sinalizador é criado pelo sistema usando dados do atributo <a href="a-pwdlastset.md"><strong>Pwd-Last-Set</strong></a> e da política de domínio. | 
| 0x01000000 | <a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a> | A conta está habilitada para delegação. Essa é uma configuração sensível à segurança; contas com essa opção habilitada devem ser estritamente controladas. Essa configuração permite que um serviço em execução na conta assuma uma identidade do cliente e se autenture como esse usuário para outros servidores remotos na rede. | 




 

