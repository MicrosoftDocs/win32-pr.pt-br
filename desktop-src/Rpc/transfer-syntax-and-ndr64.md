---
title: Sintaxe de transferência e NDR64
description: O protocolo de transmissão de NDR, também conhecido como sintaxe de transferência, permite que chamadas RPC percorram a rede.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dfec9bc1569ef9a42d0bc844c3b098736f714ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007585"
---
# <a name="transfer-syntax-and-ndr64"></a>Sintaxe de transferência e NDR64

O protocolo de transmissão de NDR, também conhecido como sintaxe de transferência, permite que chamadas RPC percorram a rede. O protocolo de transmissão define a representação de transmissão de uma chamada RPC, como a ordem na qual os membros de dados são empacotados, o alinhamento dos dados na conexão, informações adicionais incluídas nos dados e outros problemas. O protocolo NDR64 é uma extensão para a sintaxe de transferência de NDR baseada em 32 bits, criada especificamente para permitir que os desenvolvedores que visam sistemas de 64 bits obtenham um desempenho otimizado.

As diferenças entre o formato de transmissão de NDR e o formato de fio NDR64 resolvem o tamanho diferente de ponteiros em um ambiente de 64 bits, bem como outros problemas. A mecânica do NDR64 é manipulada pelo RPC. Os desenvolvedores precisam usar apenas a opção de linha de comando MIDL/[**Protocol**](/windows/desktop/Midl/-protocol)**All** para obter os benefícios do NDR64 em plataformas de 64 bits. NDR64 está disponível somente em plataformas de 64 bits.

 

 