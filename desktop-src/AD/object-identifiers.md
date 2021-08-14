---
title: Identificadores de objeto (AD DS)
description: Os OIDs (Identificadores de Objeto) são valores numéricos exclusivos emitidos por várias autoridades emissoras para identificar exclusivamente elementos de dados, sintaxes e outras partes de aplicativos distribuídos.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- identificadores de objeto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af458a003c5a5a8586c32449674019fb6b241d52c4300e107898d91c75047214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185507"
---
# <a name="object-identifiers-ad-ds"></a>Identificadores de objeto (AD DS)

Os OIDs (Identificadores de Objeto) são valores numéricos exclusivos emitidos por várias autoridades emissoras para identificar exclusivamente elementos de dados, sintaxes e outras partes de aplicativos distribuídos. Os OIDs são encontrados em aplicativos OSI, Diretórios X.500, SNMP e outros aplicativos em que a exclusividade é importante. Os OIDs se baseiam em uma estrutura de árvore, na qual uma autoridade de emissão superior, como o ISO, aloca um branch da árvore a uma subautoridade, que, por sua vez, pode alocar subbranches.

O protocolo LDAP (RFC 2251) requer um serviço de diretório para identificar classes de objeto, atributos e sintaxes com OIDs. Isso faz parte do LDAP X.500 herdado.

Os OIDs Active Directory Domain Services incluem alguns emitidos pelo ISO para classes e atributos X.500 e alguns emitidos pela Microsoft e outras autoridades emissoras. A notação OID é uma cadeia de caracteres pontilhada de números, por exemplo "1.2.840.113556.1.5.9", que é descrito na tabela a seguir.



| Valor  | Significado          | Descrição                                              |
|--------|------------------|----------------------------------------------------------|
| 1      | ISO              | Identifica a autoridade raiz.                           |
| 2      | ANSI             | Designação de grupo atribuída por ISO.                       |
| 840    | EUA              | Designação de país/região atribuída pelo grupo.        |
| 113556 | Microsoft        | Designação da organização atribuída pelo país/região. |
| 1      | Active Directory | Atribuído pela organização.                            |
| 5      | Classes          | Atribuído pela organização.                            |
| 9      | **classe de** usuário   | Atribuído pela organização.                            |



 

Para obter mais informações e uma discussão sobre dois procedimentos usados para obter OIDs válidos para uso na extensão do esquema do Active Directory, consulte Obtendo um [identificador de objeto](obtaining-an-object-identifier.md).

 

 




