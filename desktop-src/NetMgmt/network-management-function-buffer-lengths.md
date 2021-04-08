---
title: Comprimentos do buffer da função de gerenciamento de rede
description: Este tópico discute os requisitos para comprimentos de buffer de função quando usados com as APIs de gerenciamento de rede.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5003f739d235a099adb9f4f403c15c67bd9169e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822676"
---
# <a name="network-management-function-buffer-lengths"></a>Comprimentos do buffer da função de gerenciamento de rede

Este tópico discute os requisitos para comprimentos de buffer de função quando usados com as APIs de gerenciamento de rede.

Os aplicativos que especificam tamanhos de buffer ao chamar funções de enumeração de gerenciamento de rede (e várias funções de recuperação de dados) devem especificar buffers grandes o suficiente para manter a estrutura de informações retornadas (ou estruturas) Além das cadeias de caracteres às quais seus membros apontam. Se você não especificar um buffer grande o suficiente para receber todas as entradas disponíveis, a função retornará um erro com \_ mais \_ dados. As chamadas de enumeração não retornam entradas parciais.

Algumas funções de gerenciamento de rede assumem um parâmetro de comprimento máximo de dados de consultoria, *prefmaxlen*. Esse parâmetro permite que um aplicativo sugira o número de bytes que o servidor deve retornar de uma chamada de função.

Se você especificar o comprimento máximo \_ preferencial do valor \_ no parâmetro *prefmaxlen* , as funções de gerenciamento de rede alocarão a quantidade de memória necessária para os dados.

Para obter mais informações, consulte [buffers de função de gerenciamento de rede](network-management-function-buffers.md).

 

 




