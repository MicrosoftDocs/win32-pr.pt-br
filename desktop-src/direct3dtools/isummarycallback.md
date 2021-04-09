---
description: Retorno de chamada para retornar informações resumidas (exibidas na janela Propriedades).
MS-HAID: vspixengine.ISummaryCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface ISummaryCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 72B1491C-058A-480D-B3EF-AABF3C1E7D2A
api_name:
- ISummaryCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ffecd81a1bb164e50a9139552c78c1dd520e671
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087810"
---
# <a name="span-idvspixengineisummarycallbackspanisummarycallback-interface"></a><span data-ttu-id="3aa6d-103"><span id="vspixengine.isummarycallback"></span>Interface ISummaryCallback</span><span class="sxs-lookup"><span data-stu-id="3aa6d-103"><span id="vspixengine.isummarycallback"></span>ISummaryCallback interface</span></span>

<span data-ttu-id="3aa6d-104">Retorno de chamada para retornar informações resumidas (exibidas na janela Propriedades).</span><span class="sxs-lookup"><span data-stu-id="3aa6d-104">Callback to return summary information (displayed in the properties window).</span></span>

## <a name="members"></a><span data-ttu-id="3aa6d-105">Membros</span><span class="sxs-lookup"><span data-stu-id="3aa6d-105">Members</span></span>

<span data-ttu-id="3aa6d-106">A interface **ISummaryCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3aa6d-106">The **ISummaryCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3aa6d-107">**ISummaryCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3aa6d-107">**ISummaryCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="3aa6d-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="3aa6d-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="3aa6d-109"><span id="methods"></span>Maneiras</span><span class="sxs-lookup"><span data-stu-id="3aa6d-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="3aa6d-110">A interface **ISummaryCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3aa6d-110">The **ISummaryCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="3aa6d-111">Método</span><span class="sxs-lookup"><span data-stu-id="3aa6d-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="3aa6d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3aa6d-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="3aa6d-113"><a href="/windows/desktop/direct3dtools/isummarycallback-resultcallback-dword-summaryitem-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="3aa6d-113"><a href="/windows/desktop/direct3dtools/isummarycallback-resultcallback-dword-summaryitem-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="3aa6d-114">Uma função de retorno de chamada usada para notificar o host das informações de resumo do log de gráficos.</span><span class="sxs-lookup"><span data-stu-id="3aa6d-114">A callback function used to notify the host of graphics log summary information.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="3aa6d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aa6d-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3aa6d-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3aa6d-116">Header</span></span></p></td><td><span data-ttu-id="3aa6d-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3aa6d-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
