---
description: O método Render Inicializa o grafo de filtro de DVD.
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Método Render
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754752"
---
# <a name="render-method"></a><span data-ttu-id="0575e-103">Método Render</span><span class="sxs-lookup"><span data-stu-id="0575e-103">Render Method</span></span>

> [!Note]  
> <span data-ttu-id="0575e-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0575e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0575e-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="0575e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0575e-106">O `Render` método inicializa o grafo de filtro de DVD.</span><span class="sxs-lookup"><span data-stu-id="0575e-106">The `Render` method initializes the DVD filter graph.</span></span>

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a><span data-ttu-id="0575e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0575e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0575e-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*</span><span class="sxs-lookup"><span data-stu-id="0575e-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*</span></span>
</dt> <dd>

<span data-ttu-id="0575e-109">Especifica um valor inteiro que indica se o grafo de filtro será destruído e recriado.</span><span class="sxs-lookup"><span data-stu-id="0575e-109">Specifies an integer value indicating whether the filter graph will be destroyed and rebuilt.</span></span>



| <span data-ttu-id="0575e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="0575e-110">Value</span></span> | <span data-ttu-id="0575e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0575e-111">Description</span></span>                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0575e-112">0</span><span class="sxs-lookup"><span data-stu-id="0575e-112">0</span></span>     | <span data-ttu-id="0575e-113">O gráfico de filtro não será destruído e recriado se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="0575e-113">The filter graph will not be destroyed and rebuilt if it already exists.</span></span> <span data-ttu-id="0575e-114">Este é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="0575e-114">This is the default value.</span></span> |
| <span data-ttu-id="0575e-115">1</span><span class="sxs-lookup"><span data-stu-id="0575e-115">1</span></span>     | <span data-ttu-id="0575e-116">O gráfico de filtro será destruído e recriado se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="0575e-116">The filter graph will be destroyed and rebuilt if it already exists.</span></span>                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0575e-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0575e-117">Return Value</span></span>

<span data-ttu-id="0575e-118">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0575e-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0575e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="0575e-119">Remarks</span></span>

<span data-ttu-id="0575e-120">O `Render` método permite que o objeto **MSWebDVD** inicialize completamente o grafo de filtro do DirectShow subjacente na inicialização.</span><span class="sxs-lookup"><span data-stu-id="0575e-120">The `Render` method enables the **MSWebDVD** object to fully initialize the underlying DirectShow filter graph on startup.</span></span> <span data-ttu-id="0575e-121">Isso elimina o ligeiro atraso que, de outra forma, ocorre quando o usuário emite o primeiro comando para reproduzir um disco ou mostrar um menu.</span><span class="sxs-lookup"><span data-stu-id="0575e-121">This eliminates the slight delay that otherwise occurs when the user issues the first command to play a disc or show a menu.</span></span> <span data-ttu-id="0575e-122">Não há nenhum caso no qual `Render` precise ser chamado antes de chamar qualquer outro método.</span><span class="sxs-lookup"><span data-stu-id="0575e-122">There is no case in which `Render` needs to be called before calling any other method.</span></span> <span data-ttu-id="0575e-123">Por exemplo, se o aplicativo chamar [**PlayTitle**](playtitle-method.md) antes que o grafo de filtro tenha sido inicializado, o objeto **MSWebDVD** será chamado `Render` automaticamente antes de tentar reproduzir o disco.</span><span class="sxs-lookup"><span data-stu-id="0575e-123">For example, if the application calls [**PlayTitle**](playtitle-method.md) before the filter graph has been initialized, the **MSWebDVD** object calls `Render` automatically before attempting to play the disc.</span></span>

 

 



