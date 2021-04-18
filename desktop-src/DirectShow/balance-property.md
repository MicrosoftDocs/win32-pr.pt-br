---
description: A propriedade Balance define ou recupera o equilíbrio do alto-falante para a saída do fluxo de áudio.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Propriedade Balance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105760288"
---
# <a name="balance-property"></a><span data-ttu-id="5eb8c-103">Propriedade Balance</span><span class="sxs-lookup"><span data-stu-id="5eb8c-103">Balance Property</span></span>

> [!Note]  
> <span data-ttu-id="5eb8c-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5eb8c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5eb8c-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="5eb8c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5eb8c-106">A `Balance` propriedade define ou recupera o equilíbrio do alto-falante para a saída do fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="5eb8c-106">The `Balance` property sets or retrieves the speaker balance for the audio stream output.</span></span>

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a><span data-ttu-id="5eb8c-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5eb8c-107">Return Value</span></span>

<span data-ttu-id="5eb8c-108">Retorna um valor inteiro que representa os níveis de saldo.</span><span class="sxs-lookup"><span data-stu-id="5eb8c-108">Returns an integer value representing the balance levels.</span></span> <span data-ttu-id="5eb8c-109">O intervalo de entrada permitido é de-10.000 a 10.000.</span><span class="sxs-lookup"><span data-stu-id="5eb8c-109">The allowable input range is -10,000 to 10,000.</span></span> <span data-ttu-id="5eb8c-110">Um valor de 0 define um equilíbrio neutro, que é o mesmo que os alto-falantes esquerdo e direito recebem o mesmo sinal de áudio de amplitude.</span><span class="sxs-lookup"><span data-stu-id="5eb8c-110">A value of 0 sets a neutral balance, that is both left and right speakers are given the same amplitude audio signal.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eb8c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5eb8c-111">Remarks</span></span>

<span data-ttu-id="5eb8c-112">Essa propriedade é de leitura/gravação com um valor padrão de 0, o que significa que ambos os alto-falantes recebem sinais de áudio equivalentes.</span><span class="sxs-lookup"><span data-stu-id="5eb8c-112">This property is read/write with a default value of 0, meaning that both speakers receive equivalent audio signals.</span></span> <span data-ttu-id="5eb8c-113">Assim como acontece com a propriedade [**volume**](volume-property.md) , as unidades correspondem a 0,01 decibéis (multiplicado por-1 quando</span><span class="sxs-lookup"><span data-stu-id="5eb8c-113">As with the [**Volume**](volume-property.md) property, units correspond to .01 decibels (multiplied by -1 when</span></span>


```
iBalance
```



<span data-ttu-id="5eb8c-114">é um valor positivo).</span><span class="sxs-lookup"><span data-stu-id="5eb8c-114">is a positive value).</span></span> <span data-ttu-id="5eb8c-115">Por exemplo, um valor de 1000 indica 10 dB no canal direito e 90 dB no canal à esquerda.</span><span class="sxs-lookup"><span data-stu-id="5eb8c-115">For example, a value of 1000 indicates 10 dB on the right channel and 90 dB on the left channel.</span></span>

 

 



