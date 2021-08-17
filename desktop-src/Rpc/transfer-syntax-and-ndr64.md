---
title: Sintaxe de transferência e NDR64
description: O protocolo de transmissão NDR, também conhecido como sintaxe de transferência, permite que chamadas RPC percorram a rede.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433e68689ec4c960adbb43ddc19ec3e9e37765db57cfe6bf87c86c096720b771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011224"
---
# <a name="transfer-syntax-and-ndr64"></a>Sintaxe de transferência e NDR64

O protocolo de transmissão NDR, também conhecido como sintaxe de transferência, permite que chamadas RPC percorram a rede. O protocolo de transmissão define a representação de transmissão de uma chamada RPC, como a ordem em que os membros de dados são marshalados, o alinhamento dos dados na transmissão, informações adicionais incluídas nos dados e outros problemas. O protocolo NDR64 é uma extensão para a sintaxe de transferência NDR baseada em 32 bits, criada especificamente para permitir que os desenvolvedores destinados a sistemas de 64 bits alcancem o desempenho otimizado.

As diferenças entre o formato de transmissão NDR e o formato de transmissão NDR64 abordam o tamanho diferente dos ponteiros em um ambiente de 64 bits, bem como outros problemas. A mecânica de NDR64 é manipulada pelo RPC. Os desenvolvedores só precisam usar a opção de linha de comando [**/protocol**](/windows/desktop/Midl/-protocol)**all** MIDL para obter os benefícios do NDR64 em plataformas de 64 bits. O NDR64 está disponível apenas em plataformas de 64 bits.

 

 