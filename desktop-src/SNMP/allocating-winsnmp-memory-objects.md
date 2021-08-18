---
title: Alocando objetos de memória WinSNMP
description: Descritores, alças de recurso e cadeias de caracteres no estilo C são os três tipos de objetos de memória no ambiente de programação WinSNMP.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1188af74e150313cb24b01886d06df9e3ad065039cad9fa4a3e0b3b5ee6a9f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009784"
---
# <a name="allocating-winsnmp-memory-objects"></a>Alocando objetos de memória WinSNMP

Descritores, alças de recurso e cadeias de caracteres no estilo C são os três tipos de objetos de memória no ambiente de programação WinSNMP.

O tipo de objeto determina se a implementação do Microsoft WinSNMP ou o aplicativo WinSNMP aloca e desaloca a memória do objeto. Isso reduz a alocação desnecessária de espaço em buffer temporário e a cópia desnecessária de buffers.

A tabela a seguir resume a alocação e a desalocação de recursos para objetos de memória WinSNMP.



| Tipo de Objeto                                                                   | Descrição                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Descritor smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) [**ou smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) | Se o aplicativo WinSNMP alocar a memória, ele deverá desalocar a memória com uma chamada para uma função apropriada. Se a implementação alocar a memória, o aplicativo deverá chamar a [**função SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para desalocar a memória. |
| [**Estrutura smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)                                    | Se o **membro** de valor for [**um descritor smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou [**smiOCTETS,**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) o aplicativo deverá continuar conforme indicado acima para descritores.                                                                                                     |
| Alça de recurso                                                               | A implementação aloca, gerencia e libera a memória.                                                                                                                                                                                                                         |
| Cadeia de caracteres no estilo C                                                                | O aplicativo WinSNMP deve gerenciar e liberar a memória alocada.                                                                                                                                                                                                                |



 

Para obter mais informações, [consulte Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md).

 

 




