---
description: A propriedade EnableResetOnStop define ou recupera um valor que determina como a reprodução será retomada quando o grafo de filtro fizer uma transição de um estado parado.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Propriedade EnableResetOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9449d8dd3e2e5ab0e1f008cba3e4cb2aabaa78c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645936"
---
# <a name="enableresetonstop-property"></a><span data-ttu-id="73344-103">Propriedade EnableResetOnStop</span><span class="sxs-lookup"><span data-stu-id="73344-103">EnableResetOnStop Property</span></span>

> [!Note]  
> <span data-ttu-id="73344-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="73344-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="73344-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="73344-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="73344-106">A `EnableResetOnStop` propriedade define ou recupera um valor que determina como a reprodução será retomada quando o grafo de filtro fizer uma transição de um estado parado.</span><span class="sxs-lookup"><span data-stu-id="73344-106">The `EnableResetOnStop` property sets or retrieves a value that determines how play will resume when the filter graph makes a transition from a stopped state.</span></span>

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a><span data-ttu-id="73344-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="73344-107">Return Value</span></span>

<span data-ttu-id="73344-108">Retorna um valor booliano que indica onde o objeto MSWebDVD começará a ser reproduzido depois que o grafo de filtro for interrompido.</span><span class="sxs-lookup"><span data-stu-id="73344-108">Returns a Boolean value indicating where the MSWebDVD object will start playing again after the filter graph is stopped.</span></span>

## <a name="remarks"></a><span data-ttu-id="73344-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="73344-109">Remarks</span></span>

<span data-ttu-id="73344-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="73344-110">This property is read/write.</span></span>

<span data-ttu-id="73344-111">Os valores possíveis dessa propriedade são: com um valor padrão de true.</span><span class="sxs-lookup"><span data-stu-id="73344-111">The possible values of this property are: with a default value of true.</span></span>



| <span data-ttu-id="73344-112">Valor</span><span class="sxs-lookup"><span data-stu-id="73344-112">Value</span></span> | <span data-ttu-id="73344-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="73344-113">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73344-114">true</span><span class="sxs-lookup"><span data-stu-id="73344-114">true</span></span>  | <span data-ttu-id="73344-115">O navegador de DVD será reiniciado e começará a tocar desde o início do disco. Esse é o valor padrão</span><span class="sxs-lookup"><span data-stu-id="73344-115">DVD Navigator will reset and start play from the beginning of the disc. This is the default value</span></span> |
| <span data-ttu-id="73344-116">false</span><span class="sxs-lookup"><span data-stu-id="73344-116">false</span></span> | <span data-ttu-id="73344-117">O navegador de DVD retomará a reprodução de onde parou.</span><span class="sxs-lookup"><span data-stu-id="73344-117">DVD Navigator will resume play where it left off.</span></span>                                                 |



 

 

 



