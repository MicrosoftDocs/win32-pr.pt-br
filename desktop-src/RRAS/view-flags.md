---
title: Exibir sinalizadores
description: Use os sinalizadores de exibição para controlar exibições de tabela de roteamento.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5192bf3e1acaa91412d8ae7e06d035e54af1ece6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105785394"
---
# <a name="view-flags"></a>Exibir sinalizadores

Use os sinalizadores de exibição para controlar exibições de tabela de roteamento.



| Constante                 | Valor      | Descrição                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| \_tamanho máximo de \_ endereço \_ RTM | 16         | Tamanho máximo de endereço para uma família de endereços.                          |
| \_máximo de \_ exibições de RTM          | 32         | Número máximo de exibições que podem estar ativas na tabela de roteamento. |
| ID de exibição do RTM \_ \_ \_ UCAST     | 0          | Especifica uma exibição unicast.                                        |
| ID de exibição do RTM \_ \_ \_ MCast     | 1          | Especifica uma exibição de multicast.                                      |
| \_tamanho da \_ máscara de exibição RTM \_    | 0x20       | Especifica o número máximo de exibições que podem ser configuradas.    |
| \_máscara de exibição RTM \_ \_ None    | 0x00000000 | Retorna informações independentemente da exibição.                      |
| \_ \_ qualquer máscara de exibição RTM \_     | 0x00000000 | Retorna os destinos de todas as exibições. Esse é o valor padrão.  |
| \_UCAST de \_ máscara de exibição RTM \_   | 0x00000001 | Retorna os destinos da exibição unicast.                      |
| \_mcast de \_ máscara de exibição RTM \_   | 0x00000002 | Retorna os destinos da exibição multicast.                    |
| \_ \_ todas as máscaras da exibição RTM \_     | 0xFFFFFFFF | Retorna informações de todas as exibições.                              |



 

 

 




