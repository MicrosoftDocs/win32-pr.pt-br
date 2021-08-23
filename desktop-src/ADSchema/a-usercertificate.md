---
title: X509-Cert atributo
description: Contém os certificados X.509v3 codificados em DER emitidos para o usuário. Observe que essa propriedade contém os certificados de chave pública emitidos para esse usuário pelo Serviço de Certificado da Microsoft.
ms.assetid: bdd6b9a4-c402-462c-be2c-8e7e582a899a
ms.tgt_platform: multiple
keywords:
- X509-Cert atributo AD Schema
- esquema do AD do atributo userCertificate
topic_type:
- apiref
api_name:
- X509-Cert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0d6d95ab05047c19ba978a02957dca3870c2f93cf26b323bd6aa55c2f35472a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644586"
---
# <a name="x509-cert-attribute"></a>X509-Cert atributo

Contém os certificados X.509v3 codificados em DER emitidos para o usuário. Observe que essa propriedade contém os certificados de chave pública emitidos para esse usuário pelo Serviço de Certificado da Microsoft.



| Entrada | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| CN                | X509-Cert                                                                                                               |
| Ldap-Display-Name | userCertificate                                                                                                         |
| Tamanho              | Esse atributo exigirá cerca de 4 KB para cada certificado do Agente de Recuperação de Chave emitido pela AC usando a instância DEIS. |
| Privilégio de atualização  | Administrador de domínio                                                                                                    |
| Frequência de atualização  | Cada vez que um certificado é emitido.                                                                                      |
| Attribute-Id      | 2.5.4.36                                                                                                                |
| System-Id-Guid    | bf967a7f-0de6-11d0-a285-00aa003049e2                                                                                    |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                                   |



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
| Tem valor único       | Falso                                                                                  |
| É indexado             | Falso                                                                                  |
| No Catálogo Global      | Verdadeiro                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classes usadas em        | [**Destinatário do email**](c-mailrecipient.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Tem valor único       | Falso                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                              |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Tem valor único       | Falso                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                              |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Tem valor único       | Falso                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                              |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Tem valor único       | Falso                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                              |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Tem valor único       | Falso                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                              |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classes usadas em        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatário do email**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuário**](c-user.md)<br/> |



 

 





