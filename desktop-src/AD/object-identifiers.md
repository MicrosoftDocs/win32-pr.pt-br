---
title: Identificadores de objeto (AD DS)
description: Os OIDs (identificadores de objeto) são valores numéricos exclusivos emitidos por várias autoridades emissores para identificar exclusivamente elementos de dados, sintaxes e outras partes de aplicativos distribuídos.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- identificadores de objeto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2253a6173e06f5d7b0c136a520db3e1e5a5e798e
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "105748298"
---
# <a name="object-identifiers-ad-ds"></a>Identificadores de objeto (AD DS)

Os OIDs (identificadores de objeto) são valores numéricos exclusivos emitidos por várias autoridades emissores para identificar exclusivamente elementos de dados, sintaxes e outras partes de aplicativos distribuídos. Os OIDs são encontrados em aplicativos OSI, em diretórios X. 500, SNMP e em outros aplicativos onde a exclusividade é importante. Os OIDs são baseados em uma estrutura de árvore, na qual uma autoridade emissora superior, como o ISO, aloca uma ramificação da árvore para uma subautoridade que, por sua vez, pode alocar subramificações.

O protocolo LDAP (RFC 2251) requer um serviço de diretório para identificar classes de objeto, atributos e sintaxes com OIDs. Isso faz parte do herdado do LDAP X. 500.

Os OIDs em Active Directory Domain Services incluem alguns emitidos pelo ISO para classes e atributos X. 500 e alguns emitidos pela Microsoft e outras autoridades emissora. A notação OID é uma cadeia de números pontilhada, por exemplo, "1.2.840.113556.1.5.9", que é descrito na tabela a seguir.



| Valor  | Significado          | Descrição                                              |
|--------|------------------|----------------------------------------------------------|
| 1      | ISO              | Identifica a autoridade raiz.                           |
| 2      | ANSI             | Designação de grupo atribuída pela ISO.                       |
| 840    | EUA              | Designação de país/região atribuída pelo grupo.        |
| 113556 | Microsoft        | Designação de organização atribuída pelo país/região. |
| 1      | Active Directory | Atribuído pela organização.                            |
| 5      | Classes          | Atribuído pela organização.                            |
| 9      | classe de **usuário**   | Atribuído pela organização.                            |



 

Para obter mais informações e uma discussão sobre dois procedimentos usados para obter OIDs válidos para uso na extensão do esquema de Active Directory, consulte [obtendo um identificador de objeto](obtaining-an-object-identifier.md).

 

 




