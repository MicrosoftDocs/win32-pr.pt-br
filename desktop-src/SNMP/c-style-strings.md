---
title: Cadeias de caracteres C-Style
description: Um aplicativo WinSNMP pode usar cadeias de estilo C com terminação nula para converter objetos de OID (identificador de objeto e entidade) de e para suas representações de cadeia de caracteres.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6449514d4c08baae638d950a42f7f553e0037efe6bdc45b8045dbd315c1a2c65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009744"
---
# <a name="c-style-strings"></a>Cadeias de caracteres C-Style

Um aplicativo WinSNMP pode usar cadeias de estilo C com terminação **nula** para converter objetos de OID (identificador de objeto e entidade) de e para suas representações de cadeia de caracteres.

As funções WinSNMP que manipulam cadeias de caracteres em estilo C incluem [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)e [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr). Como [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) e [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) retornam um ponteiro para uma variável de cadeia de caracteres de estilo C, o aplicativo WinSNMP deve passar um valor apropriado no parâmetro *size* quando ele faz chamadas para essas funções. Para obter mais informações, consulte as páginas de referência para essas funções.

> [!Note]  
> O parâmetro de *contexto* das funções [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) e [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) deve ser uma estrutura de cadeia de caracteres de octeto, ou seja, uma estrutura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) . O parâmetro de *contexto* não pode ser uma cadeia de caracteres em estilo C. A cadeia de caracteres contida em uma estrutura **smiOCTETS** não requer um byte de terminação **nula**.

 

 

 




