---
description: Representa um Tablet anexado ao computador.
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: Interface ITablet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76fa7baea2713e5a2e5eaae562b6dac29e002fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764295"
---
# <a name="itablet-interface"></a><span data-ttu-id="8b959-103">Interface ITablet</span><span class="sxs-lookup"><span data-stu-id="8b959-103">ITablet interface</span></span>

<span data-ttu-id="8b959-104">Representa um Tablet anexado ao computador.</span><span class="sxs-lookup"><span data-stu-id="8b959-104">Represents a tablet attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="8b959-105">Membros</span><span class="sxs-lookup"><span data-stu-id="8b959-105">Members</span></span>

<span data-ttu-id="8b959-106">A interface **ITablet** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8b959-106">The **ITablet** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8b959-107">**ITablet** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8b959-107">**ITablet** also has these types of members:</span></span>

-   [<span data-ttu-id="8b959-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b959-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b959-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b959-109">Methods</span></span>

<span data-ttu-id="8b959-110">A interface **ITablet** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8b959-110">The **ITablet** interface has these methods.</span></span>



| <span data-ttu-id="8b959-111">Método</span><span class="sxs-lookup"><span data-stu-id="8b959-111">Method</span></span>                                                                 | <span data-ttu-id="8b959-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b959-112">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b959-113">**CreateContext**</span><span class="sxs-lookup"><span data-stu-id="8b959-113">**CreateContext**</span></span>](itablet-createcontext.md)                         | <span data-ttu-id="8b959-114">Cria um objeto de contexto que descreve o dispositivo tablet especificado.</span><span class="sxs-lookup"><span data-stu-id="8b959-114">Creates a context object that describes the specified tablet device.</span></span><br/>       |
| <span data-ttu-id="8b959-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b959-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span></span>                                 | <span data-ttu-id="8b959-116">Recupera o objeto [**ITabletCursor**](itabletcursor.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="8b959-116">Retrieves the specified [**ITabletCursor**](itabletcursor.md) object.</span></span><br/>     |
| [<span data-ttu-id="8b959-117">**GetCursorCount**</span><span class="sxs-lookup"><span data-stu-id="8b959-117">**GetCursorCount**</span></span>](itablet-getcursorcount.md)                       | <span data-ttu-id="8b959-118">Recupera o número de objetos de cursor associados ao Tablet.</span><span class="sxs-lookup"><span data-stu-id="8b959-118">Retrieves the number of cursor objects associated with the tablet.</span></span><br/>         |
| [<span data-ttu-id="8b959-119">**GetDefaultContextSettings**</span><span class="sxs-lookup"><span data-stu-id="8b959-119">**GetDefaultContextSettings**</span></span>](itablet-getdefaultcontextsettings.md) | <span data-ttu-id="8b959-120">Recupera as configurações de contexto padrão para o Tablet.</span><span class="sxs-lookup"><span data-stu-id="8b959-120">Retrieves the default context settings for the tablet.</span></span><br/>                     |
| [<span data-ttu-id="8b959-121">**GetHardwareCaps**</span><span class="sxs-lookup"><span data-stu-id="8b959-121">**GetHardwareCaps**</span></span>](itablet-gethardwarecaps.md)                     | <span data-ttu-id="8b959-122">Recupera um valor que representa os recursos do hardware do Tablet.</span><span class="sxs-lookup"><span data-stu-id="8b959-122">Retrieves a value that represents the capabilities of the tablet hardware.</span></span><br/> |
| [<span data-ttu-id="8b959-123">**GetMaxInputRect**</span><span class="sxs-lookup"><span data-stu-id="8b959-123">**GetMaxInputRect**</span></span>](itablet-getmaxinputrect.md)                     | <span data-ttu-id="8b959-124">Recupera um retângulo que representa a área de entrada máxima do Tablet.</span><span class="sxs-lookup"><span data-stu-id="8b959-124">Retrieves a rectangle that represents maximum input area of the tablet.</span></span><br/>    |
| [<span data-ttu-id="8b959-125">**GetName**</span><span class="sxs-lookup"><span data-stu-id="8b959-125">**GetName**</span></span>](itablet-getname.md)                                     | <span data-ttu-id="8b959-126">Recupera uma cadeia de caracteres que contém o nome do dispositivo tablet.</span><span class="sxs-lookup"><span data-stu-id="8b959-126">Retrieves a string containing the name of the tablet device.</span></span><br/>               |
| [<span data-ttu-id="8b959-127">**GetPlugAndPlayId**</span><span class="sxs-lookup"><span data-stu-id="8b959-127">**GetPlugAndPlayId**</span></span>](itablet-getplugandplayid.md)                   | <span data-ttu-id="8b959-128">Recupera uma cadeia de caracteres que contém a ID de Plug and Play para o dispositivo tablet.</span><span class="sxs-lookup"><span data-stu-id="8b959-128">Retrieves a string containing the Plug and Play ID for the tablet device.</span></span><br/>  |
| <span data-ttu-id="8b959-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b959-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span></span>               | <span data-ttu-id="8b959-130">Recupera os dados de métricas para uma propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="8b959-130">Retrieves the metrics data for a specified property.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="8b959-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b959-131">Remarks</span></span>

<span data-ttu-id="8b959-132">Os desenvolvedores não devem usar essa interface.</span><span class="sxs-lookup"><span data-stu-id="8b959-132">Developers should not use this interface.</span></span>

<span data-ttu-id="8b959-133">O código a seguir descreve como a interface **ITablet** é definida.</span><span class="sxs-lookup"><span data-stu-id="8b959-133">The following code describes how the **ITablet** interface is defined.</span></span>

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a><span data-ttu-id="8b959-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b959-134">Requirements</span></span>



| <span data-ttu-id="8b959-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b959-135">Requirement</span></span> | <span data-ttu-id="8b959-136">Valor</span><span class="sxs-lookup"><span data-stu-id="8b959-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b959-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b959-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8b959-138">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8b959-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8b959-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b959-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8b959-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8b959-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8b959-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b959-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b959-142"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b959-142"><dt>Wisptis.exe</dt></span></span> </dl> |



 

