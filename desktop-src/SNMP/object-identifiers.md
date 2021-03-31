---
title: Identificadores de objeto (SNMP)
description: Um identificador de objeto SNMP nomeia exclusivamente um objeto e identifica seu local dentro de uma estrutura de árvore de MIB (base de informações de gerenciamento).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed1f54f67b85000e508dddb42b9c784628a53ab
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644107"
---
# <a name="object-identifiers-snmp"></a>Identificadores de objeto (SNMP)

Um identificador de objeto SNMP nomeia exclusivamente um objeto e identifica seu local dentro de uma estrutura de árvore de MIB (base de informações de gerenciamento). Os identificadores de objeto são tipos de dados de notação de sintaxe abstrata independentes de aplicativo (ASN. 1) que consistem em uma sequência de números inteiros não negativos ou subidentificadores. Os identificadores de objeto devem ter um mínimo de dois subidentificadores e não devem exceder 128 subidentificadores.

O ambiente de programação WinSNMP usa a estrutura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) para gerenciar identificadores de objeto. O formato da matriz de identificador de objeto em uma estrutura **smiOID** é um subidentificador por elemento de matriz.

A representação de cadeia de caracteres numérica pontilhada de um identificador de objeto separa seus subidentificadores por períodos; por exemplo, "1.2.3.4.5.6".

Para obter mais informações, consulte [a MIB (base de informações de gerenciamento) SNMP](the-snmp-management-information-base-mib-.md) e as RFCs relevantes.

 

 




