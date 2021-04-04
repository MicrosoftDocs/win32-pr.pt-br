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
# <a name="transfer-syntax-and-ndr64"></a><span data-ttu-id="7e7be-103">Sintaxe de transferência e NDR64</span><span class="sxs-lookup"><span data-stu-id="7e7be-103">Transfer Syntax and NDR64</span></span>

<span data-ttu-id="7e7be-104">O protocolo de transmissão de NDR, também conhecido como sintaxe de transferência, permite que chamadas RPC percorram a rede.</span><span class="sxs-lookup"><span data-stu-id="7e7be-104">The NDR wire protocol, also referred to as transfer syntax, enables RPC calls to traverse the network.</span></span> <span data-ttu-id="7e7be-105">O protocolo de transmissão define a representação de transmissão de uma chamada RPC, como a ordem na qual os membros de dados são empacotados, o alinhamento dos dados na conexão, informações adicionais incluídas nos dados e outros problemas.</span><span class="sxs-lookup"><span data-stu-id="7e7be-105">The wire protocol defines the wire representation of an RPC call, such as the order in which data members are marshaled, alignment of data on the wire, additional information included with the data, and other issues.</span></span> <span data-ttu-id="7e7be-106">O protocolo NDR64 é uma extensão para a sintaxe de transferência de NDR baseada em 32 bits, criada especificamente para permitir que os desenvolvedores que visam sistemas de 64 bits obtenham um desempenho otimizado.</span><span class="sxs-lookup"><span data-stu-id="7e7be-106">The NDR64 protocol is an extension to the 32-bit based NDR transfer syntax, created specifically to enable developers targeting 64-bit systems to achieve optimized performance.</span></span>

<span data-ttu-id="7e7be-107">As diferenças entre o formato de transmissão de NDR e o formato de fio NDR64 resolvem o tamanho diferente de ponteiros em um ambiente de 64 bits, bem como outros problemas.</span><span class="sxs-lookup"><span data-stu-id="7e7be-107">The differences between the NDR wire format and the NDR64 wire format addresses the different size of pointers in a 64-bit environment, as well as other issues.</span></span> <span data-ttu-id="7e7be-108">A mecânica do NDR64 é manipulada pelo RPC.</span><span class="sxs-lookup"><span data-stu-id="7e7be-108">The mechanics of NDR64 is handled by RPC.</span></span> <span data-ttu-id="7e7be-109">Os desenvolvedores precisam usar apenas a opção de linha de comando MIDL/[**Protocol**](/windows/desktop/Midl/-protocol)**All** para obter os benefícios do NDR64 em plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7e7be-109">Developers need only use the /[**protocol**](/windows/desktop/Midl/-protocol)**all** MIDL command line switch to obtain the benefits of NDR64 on 64-bit platforms.</span></span> <span data-ttu-id="7e7be-110">NDR64 está disponível somente em plataformas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7e7be-110">NDR64 is available only on 64-bit platforms.</span></span>

 

 