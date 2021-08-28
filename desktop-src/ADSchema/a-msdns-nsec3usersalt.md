---
title: Atributo ms-DNS-NSEC3-User-Salt
description: Um atributo que define uma cadeia de caracteres de sal NSEC3 especificada pelo usuário a ser usada ao assinar a zona DNS. Se estiver vazio, o sal aleatório será usado.
ms.assetid: b9829732-8a79-4f07-8644-9fe4ba05ba8f
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo ms-DNS-NSEC3-User-Salt
- Esquema do AD do atributo msDNS-NSEC3UserSalt
topic_type:
- apiref
api_name:
- ms-DNS-NSEC3-User-Salt
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dbd1725675487ae5a6812dd77c400745b6671de0ef7db360e1c1980dd25b1b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553016"
---
# <a name="ms-dns-nsec3-user-salt-attribute"></a>Atributo ms-DNS-NSEC3-User-Salt

Um atributo que define uma cadeia de caracteres de sal NSEC3 especificada pelo usuário a ser usada ao assinar a zona DNS. Se estiver vazio, o sal aleatório será usado.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | ms-DNS-NSEC3-User-Salt                      |
| Ldap-Display-Name | msDNS-NSEC3UserSalt                         |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.2148                     |
| System-Id-Guid    | aff16770-9622-4fbc-a128-3088777605b9        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| Tem valor único       | Verdadeiro                                     |
| É indexado             | Falso                                    |
| No Catálogo Global      | Falso                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                             |
| Range-Lower            | 0                                        |
| Range-Upper            | 510                                      |
| Search-Flags           | 0x00000008                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**Zona DNS**](c-dnszone.md)<br/> |



 

 





