---
title: Estruturas de WinSNMP
description: As funções de API WinSNMP usam as seguintes estruturas.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- Estruturas de WinSNMP SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823865"
---
# <a name="winsnmp-structures"></a>Estruturas de WinSNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

As funções de API WinSNMP usam as seguintes estruturas.



| Estrutura                                  | Descrição                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**smiCNTR64**](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | Contém um valor inteiro sem sinal de 64 bits que representa um contador.                                                    |
| [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | Contém um ponteiro para uma cadeia de caracteres de octeto SNMP de comprimento variável.                                                         |
| [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | Contém um ponteiro para uma matriz de comprimento variável dos subidentificadores associados a um objeto nomeado especificado. |
| [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | Representa o valor associado a um nome de variável em uma entrada de associação de variável.                              |
| [**smiVENDORINFO**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | Contém informações sobre a implementação da Microsoft de WinSNMP.                                                    |



 

 

 