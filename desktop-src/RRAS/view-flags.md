---
title: Exibir sinalizadores
description: Use Os sinalizadores de exibição para controlar as exibições da tabela de roteamento.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ae9763587cf7972aab3ca9880d5ad26350c3161955c17940484cc1cbd801bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024946"
---
# <a name="view-flags"></a>Exibir sinalizadores

Use Os sinalizadores de exibição para controlar as exibições da tabela de roteamento.



| Constante                 | Valor      | Descrição                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| TAMANHO MÁXIMO \_ \_ DO ENDEREÇO RTM \_ | 16         | Tamanho máximo do endereço para uma família de endereços.                          |
| EXIBIÇÕES DE RTM \_ \_ MAX          | 32         | Número máximo de exibições que podem estar ativas na tabela de roteamento. |
| \_ \_ UCAST da ID DE EXIBIÇÃO \_ RTM     | 0          | Especifica uma exibição unicast.                                        |
| MCAST \_ \_ da ID DE EXIBIÇÃO \_ RTM     | 1          | Especifica uma exibição multicast.                                      |
| TAMANHO DA \_ MÁSCARA DE \_ EXIBIÇÃO RTM \_    | 0x20       | Especifica o número máximo de exibições que podem ser configuradas.    |
| MÁSCARA DE EXIBIÇÃO RTM \_ \_ \_ NONE    | 0x00000000 | Retorna informações, independentemente da exibição.                      |
| MÁSCARA DE \_ \_ EXIBIÇÃO RTM \_ ANY     | 0x00000000 | Retorna destinos de todas as exibições. Esse é o valor padrão.  |
| MÁSCARA DE \_ \_ EXIBIÇÃO \_ RTM UCAST   | 0x00000001 | Retorna destinos da exibição unicast.                      |
| MCAST \_ DA MÁSCARA DE \_ \_ EXIBIÇÃO RTM   | 0x00000002 | Retorna destinos da exibição multicast.                    |
| MÁSCARA DE EXIBIÇÃO RTM \_ \_ \_ ALL     | 0xFFFFFFFF | Retorna informações de todas as exibições.                              |



 

 

 




