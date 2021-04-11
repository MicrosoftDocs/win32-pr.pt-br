---
title: Atributo de controle de conta de usuário
description: Sinalizadores que controlam o comportamento da conta de usuário.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo de controle de conta de usuário
- Esquema do AD do atributo userAccountControl
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f60297d22aad76b229c691a667ac22a87271402c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086977"
---
# <a name="user-account-control-attribute"></a>Atributo de controle de conta de usuário

Sinalizadores que controlam o comportamento da conta de usuário.



| Entrada | Valor |
|-------------------|---------------------------------------|
| CN                | Controle de conta de usuário                  |
| LDAP-Display-Name | userAccountControl                    |
| Tamanho              | 4 bytes.                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.      |
| Frequência de atualização  | Cada vez que a política de conta é alterada. |
| Attribute-Id      | 1.2.840.113556.1.4.8                  |
| System-ID-GUID    | bf967a68-0de6-11d0-a285-00aa003049e2  |
| Syntax            | [**Enumeração**](s-enumeration.md)  |



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
| É de valor único       | True                              |
| É indexado             | True                              |
| No catálogo global      | True                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
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
| É de valor único       | True                              |
| É indexado             | True                              |
| No catálogo global      | True                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
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
| É de valor único       | True                              |
| É indexado             | True                              |
| No catálogo global      | True                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
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
| É de valor único       | True                              |
| É indexado             | True                              |
| No catálogo global      | True                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
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
| É de valor único       | True                              |
| É indexado             | True                              |
| No catálogo global      | True                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
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
| É de valor único       | True                              |
| É indexado             | True                              |
| No catálogo global      | True                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="remarks"></a>Comentários

Esse valor de atributo pode ser zero ou uma combinação de um ou mais dos valores a seguir.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor hexadecimal</th>
<th>Identificador (definido em IADs. h)</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x00000001</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></td>
<td>O script de logon é executado.</td>
</tr>
<tr class="even">
<td>0x00000002</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></td>
<td>A conta de usuário está desabilitada.</td>
</tr>
<tr class="odd">
<td>0x00000008</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></td>
<td>O diretório base é necessário.</td>
</tr>
<tr class="even">
<td>0x00000010</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></td>
<td>A conta está bloqueada no momento.</td>
</tr>
<tr class="odd">
<td>0x00000020</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></td>
<td>Nenhuma senha é necessária.</td>
</tr>
<tr class="even">
<td>0x00000040</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></td>
<td>O usuário não pode alterar a senha.
<blockquote>
[!Note]<br />
Você não pode atribuir as configurações de permissão de PASSWD_CANT_CHANGE modificando diretamente o atributo UserAccountControl. Para obter mais informações e um exemplo de código que mostra como impedir que um usuário altere a senha, consulte o <a href="/windows/desktop/ADSI/user-cannot-change-password">usuário não pode alterar a senha</a>.
</blockquote>
<br/> :</td>
</tr>
<tr class="odd">
<td>0x00000080</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></td>
<td>O usuário pode enviar uma senha criptografada.</td>
</tr>
<tr class="even">
<td>0x00000100</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></td>
<td>Essa é uma conta para usuários cuja conta primária está em outro domínio. Essa conta fornece acesso de usuário a esse domínio, mas não a qualquer domínio que confie nesse domínio. Também conhecido como uma conta de usuário local.</td>
</tr>
<tr class="odd">
<td>0x00000200</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></td>
<td>Esse é um tipo de conta padrão que representa um usuário típico.</td>
</tr>
<tr class="even">
<td>0x00000800</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></td>
<td>Essa é uma permissão para confiar na conta de um domínio do sistema que confia em outros domínios.</td>
</tr>
<tr class="odd">
<td>0x00001000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></td>
<td>Esta é uma conta de computador para um computador que seja membro deste domínio.</td>
</tr>
<tr class="even">
<td>0x00002000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></td>
<td>Essa é uma conta de computador para um controlador de domínio de backup do sistema que é membro deste domínio.</td>
</tr>
<tr class="odd">
<td>0x00004000</td>
<td>N/D</td>
<td>Não usado.</td>
</tr>
<tr class="even">
<td>0x00008000</td>
<td>N/D</td>
<td>Não usado.</td>
</tr>
<tr class="odd">
<td>0x00010000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></td>
<td>A senha desta conta nunca expirará.</td>
</tr>
<tr class="even">
<td>0x00020000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></td>
<td>Esta é uma conta de logon MNS.</td>
</tr>
<tr class="odd">
<td>0x00040000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></td>
<td>O usuário deve fazer logon usando um cartão inteligente.</td>
</tr>
<tr class="even">
<td>0x00080000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></td>
<td>A conta de serviço (conta de usuário ou de computador), sob a qual um serviço é executado, é confiável para delegação de Kerberos. Qualquer serviço desse tipo pode representar um cliente solicitando o serviço.</td>
</tr>
<tr class="odd">
<td>0x00100000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></td>
<td>O contexto de segurança do usuário não será delegado a um serviço, mesmo que a conta de serviço esteja definida como confiável para delegação de Kerberos.</td>
</tr>
<tr class="even">
<td>0x00200000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></td>
<td>Restrinja esta entidade para usar apenas os tipos de criptografia DES (padrão de criptografia de dados) para chaves.</td>
</tr>
<tr class="odd">
<td>0x00400000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></td>
<td>Essa conta não requer pré-autenticação Kerberos para logon.</td>
</tr>
<tr class="even">
<td>0x00800000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></td>
<td>A senha do usuário expirou. Esse sinalizador é criado pelo sistema usando dados do atributo <a href="a-pwdlastset.md"><strong>pwd-Last-Set</strong></a> e da política de domínio.</td>
</tr>
<tr class="odd">
<td>0x01000000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></td>
<td>A conta está habilitada para delegação. Esta é uma configuração sensível à segurança; as contas com essa opção habilitada devem ser estritamente controladas. Essa configuração permite que um serviço em execução na conta assuma uma identidade do cliente e se autentique como esse usuário para outros servidores remotos na rede.</td>
</tr>
</tbody>
</table>



 

