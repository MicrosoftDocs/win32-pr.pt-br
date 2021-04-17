---
description: Retorno de chamada para retornar as versões de todas as interfaces com suporte. Isso permite que o consumidor fique fora de sincronia com o mecanismo de captura.
MS-HAID: vspixengine.IVersionCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IVersionCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7135E175-C537-4B0C-8F0A-CB77E3F2D945
api_name:
- IVersionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c53008e625d63e2e876bef9ab8cbdd376508c2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105813754"
---
# <a name="span-idvspixengineiversioncallbackspaniversioncallback-interface"></a><span data-ttu-id="75ecc-104"><span id="vspixengine.iversioncallback"></span>Interface IVersionCallback</span><span class="sxs-lookup"><span data-stu-id="75ecc-104"><span id="vspixengine.iversioncallback"></span>IVersionCallback interface</span></span>

<span data-ttu-id="75ecc-105">Retorno de chamada para retornar as versões de todas as interfaces com suporte.</span><span class="sxs-lookup"><span data-stu-id="75ecc-105">Callback to return the versions of all the interfaces supported.</span></span> <span data-ttu-id="75ecc-106">Isso permite que o consumidor fique fora de sincronia com o mecanismo de captura.</span><span class="sxs-lookup"><span data-stu-id="75ecc-106">This allows the consumer to be out of sync with the capture engine.</span></span>

## <a name="members"></a><span data-ttu-id="75ecc-107">Membros</span><span class="sxs-lookup"><span data-stu-id="75ecc-107">Members</span></span>

<span data-ttu-id="75ecc-108">A interface **IVersionCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="75ecc-108">The **IVersionCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="75ecc-109">**IVersionCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="75ecc-109">**IVersionCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="75ecc-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="75ecc-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="75ecc-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="75ecc-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="75ecc-112">A interface **IVersionCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="75ecc-112">The **IVersionCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="75ecc-113">Método</span><span class="sxs-lookup"><span data-stu-id="75ecc-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="75ecc-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="75ecc-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="75ecc-115"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ecc-115"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="75ecc-116">Uma função de retorno de chamada usada para notificar o host de quais interfaces têm suporte.</span><span class="sxs-lookup"><span data-stu-id="75ecc-116">A callback function used to notify the host of which interfaces are supported.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="75ecc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75ecc-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="75ecc-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75ecc-118">Header</span></span></p></td><td><span data-ttu-id="75ecc-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="75ecc-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
