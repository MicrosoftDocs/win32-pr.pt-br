---
description: Retorno de chamada para retornar dados da tabela de objetos.
MS-HAID: vspixengine.IObjectTableCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IObjectTableCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D3B5ECD5-DBE1-4E37-8707-CFAEFEE551F1
api_name:
- IObjectTableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4535164048c92e6af381d15ee388212fdc72da4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088789"
---
# <a name="span-idvspixengineiobjecttablecallbackspaniobjecttablecallback-interface"></a><span data-ttu-id="76061-103"><span id="vspixengine.iobjecttablecallback"></span>Interface IObjectTableCallback</span><span class="sxs-lookup"><span data-stu-id="76061-103"><span id="vspixengine.iobjecttablecallback"></span>IObjectTableCallback interface</span></span>

<span data-ttu-id="76061-104">Retorno de chamada para retornar dados da tabela de objetos.</span><span class="sxs-lookup"><span data-stu-id="76061-104">Callback to return object table data.</span></span>

## <a name="members"></a><span data-ttu-id="76061-105">Membros</span><span class="sxs-lookup"><span data-stu-id="76061-105">Members</span></span>

<span data-ttu-id="76061-106">A interface **IObjectTableCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="76061-106">The **IObjectTableCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="76061-107">**IObjectTableCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="76061-107">**IObjectTableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="76061-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="76061-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="76061-109"><span id="methods"></span>Maneiras</span><span class="sxs-lookup"><span data-stu-id="76061-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="76061-110">A interface **IObjectTableCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="76061-110">The **IObjectTableCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="76061-111">Método</span><span class="sxs-lookup"><span data-stu-id="76061-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="76061-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="76061-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="76061-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></span><span class="sxs-lookup"><span data-stu-id="76061-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="76061-114">Obtém informações sobre quais colunas (tipos de dados de objeto) têm suporte na tabela de objetos.</span><span class="sxs-lookup"><span data-stu-id="76061-114">Gets information about which columns (types of object data) are supported by the object table.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="76061-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="76061-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="76061-116">Uma função de retorno de chamada usada para notificar o host das informações da tabela de objetos.</span><span class="sxs-lookup"><span data-stu-id="76061-116">A callback function used to notify the host of object table information.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="76061-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76061-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="76061-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76061-118">Header</span></span></p></td><td><span data-ttu-id="76061-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="76061-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
