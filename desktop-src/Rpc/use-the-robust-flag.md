---
title: Usar o sinalizador/robust
description: Sempre compile arquivos. idl usando a opção/robust
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db395841842331d9297a782fdcd8ea7573139f9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917443"
---
# <a name="use-the-robust-flag"></a><span data-ttu-id="c9e1f-103">Usar o sinalizador/robust</span><span class="sxs-lookup"><span data-stu-id="c9e1f-103">Use the /robust Flag</span></span>

<span data-ttu-id="c9e1f-104">Sempre compile arquivos. idl usando a opção [**/robust**](/windows/desktop/Midl/-robust)</span><span class="sxs-lookup"><span data-stu-id="c9e1f-104">Always compile .idl files using the [**/robust**](/windows/desktop/Midl/-robust) switch.</span></span> <span data-ttu-id="c9e1f-105">O uso da opção **/robust** gera informações adicionais que permitem que o mecanismo de representação de dados de rede (NDR) execute a verificação de erros em tempo de execução em argumentos correlacionados em matrizes dinâmicas, uniões e ponteiros de interface em aplicativos com e RPC.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-105">Using the **/robust** switch generates additional information that enables the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in out interface pointers in COM and RPC applications.</span></span> <span data-ttu-id="c9e1f-106">Se o software não conseguir compilar com esse sinalizador, o software será tão exposto a ataques que nenhum esforço em nenhuma outra área poderá protegê-lo.</span><span class="sxs-lookup"><span data-stu-id="c9e1f-106">If software fails to compile with this flag, the software is so exposed to attacks that no efforts in any other area can protect it.</span></span>

 

 