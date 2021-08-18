---
title: Estruturas WinSNMP
description: As funções da API WinSNMP usam as estruturas a seguir.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- Estruturas WinSNMP SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b409b6d12063ebd3feb9c663f2d607bc5ceead0462b2945334f1e7e691c9be63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142749"
---
# <a name="winsnmp-structures"></a>Estruturas WinSNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, [Windows gerenciamento remoto,](/windows/desktop/WinRM/portal)que é a implementação da Microsoft do WS-Man.\]

As funções da API WinSNMP usam as estruturas a seguir.



| Estrutura                                  | Descrição                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**smiCNTR64**](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | Contém um valor inteiro sem sinal de 64 bits que representa um contador.                                                    |
| [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | Contém um ponteiro para uma cadeia de caracteres de octeto SNMP de comprimento variável.                                                         |
| [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | Contém um ponteiro para uma matriz de comprimento variável dos subidentificadores associados a um objeto nomeado especificado. |
| [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | Representa o valor associado a um nome de variável em uma entrada de associação de variável.                              |
| [**smiVENDORINFO**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | Contém informações sobre a implementação da Microsoft do WinSNMP.                                                    |



 

 

 