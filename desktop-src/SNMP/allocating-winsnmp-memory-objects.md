---
title: Alocando objetos de memória WinSNMP
description: Os descritores, os identificadores de recursos e as cadeias de caracteres em estilo C são os três tipos de objetos de memória no ambiente de programação WinSNMP.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70ed4d9d52452b5067a6d1e51392b84f95ccce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004844"
---
# <a name="allocating-winsnmp-memory-objects"></a>Alocando objetos de memória WinSNMP

Os descritores, os identificadores de recursos e as cadeias de caracteres em estilo C são os três tipos de objetos de memória no ambiente de programação WinSNMP.

O tipo de objeto determina se a implementação de WinSNMP da Microsoft ou o aplicativo WinSNMP aloca e anula a memória para o objeto. Isso reduz a alocação desnecessária do espaço de buffer temporário e a cópia desnecessária de buffers.

A tabela a seguir resume a alocação e a desalocação de recursos para objetos de memória WinSNMP.



| Tipo de Objeto                                                                   | Descrição                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| descritor [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) | Se o aplicativo WinSNMP alocar a memória, ele deverá desalocar a memória com uma chamada para uma função apropriada. Se a implementação alocar a memória, o aplicativo deverá chamar a função [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para desalocar a memória. |
| estrutura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)                                    | Se o membro de **valor** for um descritor [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , o aplicativo deverá continuar conforme indicado acima para os descritores.                                                                                                     |
| Identificador de recursos                                                               | A implementação aloca, gerencia e libera a memória.                                                                                                                                                                                                                         |
| Cadeia de caracteres C-Style                                                                | O aplicativo WinSNMP deve gerenciar e liberar a memória alocada.                                                                                                                                                                                                                |



 

Para obter mais informações, consulte [liberando descritores de WinSNMP](freeing-winsnmp-descriptors.md).

 

 




