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
# <a name="network-management-function-buffer-lengths"></a><span data-ttu-id="fac45-103">Comprimentos do buffer da função de gerenciamento de rede</span><span class="sxs-lookup"><span data-stu-id="fac45-103">Network Management Function Buffer Lengths</span></span>

<span data-ttu-id="fac45-104">Este tópico discute os requisitos para comprimentos de buffer de função quando usados com as APIs de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="fac45-104">This topic discusses the requirements for function buffer lengths when used with the network management APIs.</span></span>

<span data-ttu-id="fac45-105">Os aplicativos que especificam tamanhos de buffer ao chamar funções de enumeração de gerenciamento de rede (e várias funções de recuperação de dados) devem especificar buffers grandes o suficiente para manter a estrutura de informações retornadas (ou estruturas) Além das cadeias de caracteres às quais seus membros apontam.</span><span class="sxs-lookup"><span data-stu-id="fac45-105">Applications that specify buffer sizes when calling network management enumeration functions (and various data retrieval functions) must specify buffers large enough to hold the returned information structure (or structures) plus the strings to which their members point.</span></span> <span data-ttu-id="fac45-106">Se você não especificar um buffer grande o suficiente para receber todas as entradas disponíveis, a função retornará um erro com \_ mais \_ dados.</span><span class="sxs-lookup"><span data-stu-id="fac45-106">If you do not specify a large enough buffer to receive all the available entries, the function returns ERROR\_MORE\_DATA.</span></span> <span data-ttu-id="fac45-107">As chamadas de enumeração não retornam entradas parciais.</span><span class="sxs-lookup"><span data-stu-id="fac45-107">Enumeration calls do not return partial entries.</span></span>

<span data-ttu-id="fac45-108">Algumas funções de gerenciamento de rede assumem um parâmetro de comprimento máximo de dados de consultoria, *prefmaxlen*.</span><span class="sxs-lookup"><span data-stu-id="fac45-108">Some network management functions take an advisory maximum data-length parameter, *prefmaxlen*.</span></span> <span data-ttu-id="fac45-109">Esse parâmetro permite que um aplicativo sugira o número de bytes que o servidor deve retornar de uma chamada de função.</span><span class="sxs-lookup"><span data-stu-id="fac45-109">This parameter allows an application to suggest the number of bytes the server should return from a function call.</span></span>

<span data-ttu-id="fac45-110">Se você especificar o comprimento máximo \_ preferencial do valor \_ no parâmetro *prefmaxlen* , as funções de gerenciamento de rede alocarão a quantidade de memória necessária para os dados.</span><span class="sxs-lookup"><span data-stu-id="fac45-110">If you specify the value MAX\_PREFERRED\_LENGTH in the *prefmaxlen* parameter, the network management functions allocate the amount of memory required for the data.</span></span>

<span data-ttu-id="fac45-111">Para obter mais informações, consulte [buffers de função de gerenciamento de rede](network-management-function-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="fac45-111">For more information, see [Network Management Function Buffers](network-management-function-buffers.md).</span></span>

 

 




