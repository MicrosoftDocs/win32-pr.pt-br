---
description: A propriedade PlayState recupera o estado atual do objeto MSWebDVD.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Propriedade PlayState
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757872"
---
# <a name="playstate-property"></a><span data-ttu-id="fc6de-103">Propriedade PlayState</span><span class="sxs-lookup"><span data-stu-id="fc6de-103">PlayState Property</span></span>

> [!Note]  
> <span data-ttu-id="fc6de-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fc6de-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fc6de-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="fc6de-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fc6de-106">A `PlayState` propriedade recupera o estado atual do objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="fc6de-106">The `PlayState` property retrieves the current state of the **MSWebDVD** object.</span></span>

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a><span data-ttu-id="fc6de-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fc6de-107">Return Value</span></span>

<span data-ttu-id="fc6de-108">Retorna um valor inteiro que representa o estado atual do navegador de DVD.</span><span class="sxs-lookup"><span data-stu-id="fc6de-108">Returns an Integer value representing the current state of the DVD Navigator.</span></span>



| <span data-ttu-id="fc6de-109">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fc6de-109">Return code</span></span> | <span data-ttu-id="fc6de-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc6de-110">Description</span></span>   |
|-------------|---------------|
| <span data-ttu-id="fc6de-111">-2</span><span class="sxs-lookup"><span data-stu-id="fc6de-111">-2</span></span>          | <span data-ttu-id="fc6de-112">Indefinido</span><span class="sxs-lookup"><span data-stu-id="fc6de-112">Undefined</span></span>     |
| <span data-ttu-id="fc6de-113">-1</span><span class="sxs-lookup"><span data-stu-id="fc6de-113">-1</span></span>          | <span data-ttu-id="fc6de-114">Não Inicializado</span><span class="sxs-lookup"><span data-stu-id="fc6de-114">Uninitialized</span></span> |
| <span data-ttu-id="fc6de-115">0</span><span class="sxs-lookup"><span data-stu-id="fc6de-115">0</span></span>           | <span data-ttu-id="fc6de-116">Parado</span><span class="sxs-lookup"><span data-stu-id="fc6de-116">Stopped</span></span>       |
| <span data-ttu-id="fc6de-117">1</span><span class="sxs-lookup"><span data-stu-id="fc6de-117">1</span></span>           | <span data-ttu-id="fc6de-118">Em Pausa</span><span class="sxs-lookup"><span data-stu-id="fc6de-118">Paused</span></span>        |
| <span data-ttu-id="fc6de-119">2</span><span class="sxs-lookup"><span data-stu-id="fc6de-119">2</span></span>           | <span data-ttu-id="fc6de-120">Executando</span><span class="sxs-lookup"><span data-stu-id="fc6de-120">Running</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="fc6de-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc6de-121">Remarks</span></span>

<span data-ttu-id="fc6de-122">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="fc6de-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="fc6de-123">O objeto **MSWebDVD** controla o filtro de navegador de DVD do DirectShow, que faz o trabalho real de navegação em DVD.</span><span class="sxs-lookup"><span data-stu-id="fc6de-123">The **MSWebDVD** object controls the DirectShow DVD Navigator filter, which does the actual work of DVD navigation.</span></span> <span data-ttu-id="fc6de-124">Na verdade, é o estado do navegador de DVD ao qual essa propriedade se refere.</span><span class="sxs-lookup"><span data-stu-id="fc6de-124">It is actually the state of the DVD Navigator that this property refers to.</span></span> <span data-ttu-id="fc6de-125">O navegador de DVD pode estar em um dos vários Estados, conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="fc6de-125">The DVD Navigator can be in one of several states, as described above.</span></span> <span data-ttu-id="fc6de-126">A `PlayState` propriedade pode ser útil como uma ferramenta de diagnóstico, mas, em geral, não deve haver motivo para um aplicativo de script monitorar o estado do navegador de DVD.</span><span class="sxs-lookup"><span data-stu-id="fc6de-126">The `PlayState` property can be useful as a diagnostic tool, but generally there should be no reason for a scripting application to monitor the state of the DVD Navigator.</span></span>

 

 



