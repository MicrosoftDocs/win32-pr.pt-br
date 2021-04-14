---
title: X509-Cert atributo
description: Contém os certificados X. 509v3 codificados em DER emitidos para o usuário. Observe que essa propriedade contém os certificados de chave pública emitidos para esse usuário pelo serviço de certificado da Microsoft.
ms.assetid: bdd6b9a4-c402-462c-be2c-8e7e582a899a
ms.tgt_platform: multiple
keywords:
- Esquema de X509-Cert do atributo AD
- Esquema de AD do atributo userCertificate
topic_type:
- apiref
api_name:
- X509-Cert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa6f0dfb5acc25890361a124e52b8b24958915f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456245"
---
# <a name="x509-cert-attribute"></a>X509-Cert atributo

Contém os certificados X. 509v3 codificados em DER emitidos para o usuário. Observe que essa propriedade contém os certificados de chave pública emitidos para esse usuário pelo serviço de certificado da Microsoft.



| Entrada | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| CN                | X509-Cert                                                                                                               |
| LDAP-Display-Name | userCertificate                                                                                                         |
| Tamanho              | Esse atributo exigirá cerca de 4 KB para cada certificado de agente de recuperação de chave emitido pela autoridade de certificação usando a instância de KRA. |
| Privilégio de atualização  | Administrador de domínio                                                                                                    |
| Frequência de atualização  | Cada vez que um certificado é emitido.                                                                                      |
| Attribute-Id      | 2.5.4.36                                                                                                                |
| System-ID-GUID    | bf967a7f-0de6-11d0-a285-00aa003049e2                                                                                    |
| Syntax            | [**Objeto (link de réplica)**](s-object-replica-link.md)                                                                   |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                     |
| MAPI-Id                | 0x8C6A                                                                                 |
| System-Only            | Falso                                                                                  |
| É de valor único       | Falso                                                                                  |
| É indexado             | Falso                                                                                  |
| No catálogo global      | True                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classes usadas em        | [**Destinatário de email**](c-mailrecipient.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| É de valor único       | Falso                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                              |
| No catálogo global      | True                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| É de valor único       | Falso                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                              |
| No catálogo global      | True                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| É de valor único       | Falso                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                              |
| No catálogo global      | True                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| É de valor único       | Falso                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                              |
| No catálogo global      | True                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| É de valor único       | Falso                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                              |
| No catálogo global      | True                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatário de email**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





