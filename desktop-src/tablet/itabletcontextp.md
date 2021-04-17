---
description: Representa o contexto do Tablet.
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: Interface ITabletContextP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5b3b6a69deeaa30c3fa0e16b1b36094dceaff304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812071"
---
# <a name="itabletcontextp-interface"></a><span data-ttu-id="12ba6-103">Interface ITabletContextP</span><span class="sxs-lookup"><span data-stu-id="12ba6-103">ITabletContextP interface</span></span>

<span data-ttu-id="12ba6-104">Representa o contexto do Tablet.</span><span class="sxs-lookup"><span data-stu-id="12ba6-104">Represents the tablet context.</span></span>

## <a name="members"></a><span data-ttu-id="12ba6-105">Membros</span><span class="sxs-lookup"><span data-stu-id="12ba6-105">Members</span></span>

<span data-ttu-id="12ba6-106">A interface **ITabletContextP** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="12ba6-106">The **ITabletContextP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="12ba6-107">**ITabletContextP** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="12ba6-107">**ITabletContextP** also has these types of members:</span></span>

-   [<span data-ttu-id="12ba6-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="12ba6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="12ba6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="12ba6-109">Methods</span></span>

<span data-ttu-id="12ba6-110">A interface **ITabletContextP** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="12ba6-110">The **ITabletContextP** interface has these methods.</span></span>



| <span data-ttu-id="12ba6-111">Método</span><span class="sxs-lookup"><span data-stu-id="12ba6-111">Method</span></span>                                                                                           | <span data-ttu-id="12ba6-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="12ba6-112">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="12ba6-113">**IsTopMostHook**</span><span class="sxs-lookup"><span data-stu-id="12ba6-113">**IsTopMostHook**</span></span>](itabletcontextp-istopmosthook.md)                                           | <span data-ttu-id="12ba6-114">Indica se o contexto do Tablet está na parte superior do gancho.</span><span class="sxs-lookup"><span data-stu-id="12ba6-114">Indicates if the tablet context is in the top most hook.</span></span><br/>             |
| [<span data-ttu-id="12ba6-115">**Post**</span><span class="sxs-lookup"><span data-stu-id="12ba6-115">**Overlap**</span></span>](itabletcontextp-overlap.md)                                                       | <span data-ttu-id="12ba6-116">Move um contexto do Tablet para a frente ou para trás da fila de entrada.</span><span class="sxs-lookup"><span data-stu-id="12ba6-116">Moves a tablet context to the front or back of the input queue.</span></span><br/>      |
| [<span data-ttu-id="12ba6-117">**TrackInputRect**</span><span class="sxs-lookup"><span data-stu-id="12ba6-117">**TrackInputRect**</span></span>](itabletcontextp-trackinputrect.md)                                         | <span data-ttu-id="12ba6-118">Atualiza o Tablet digitalizador para as coordenadas de mapeamento de local de janela.</span><span class="sxs-lookup"><span data-stu-id="12ba6-118">Updates the tablet digitizer to window location mapping coordinates.</span></span><br/> |
| [<span data-ttu-id="12ba6-119">**UseNamedSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="12ba6-119">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md) | <span data-ttu-id="12ba6-120">Fornece acesso à memória compartilhada entre threads do Tablet.</span><span class="sxs-lookup"><span data-stu-id="12ba6-120">Provides access to memory shared between tablet threads.</span></span><br/>             |
| [<span data-ttu-id="12ba6-121">**UseSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="12ba6-121">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)           | <span data-ttu-id="12ba6-122">Fornece acesso à memória compartilhada entre threads do Tablet.</span><span class="sxs-lookup"><span data-stu-id="12ba6-122">Provides access to memory shared between tablet threads.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="12ba6-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="12ba6-123">Remarks</span></span>

<span data-ttu-id="12ba6-124">Os desenvolvedores não devem usar essa interface.</span><span class="sxs-lookup"><span data-stu-id="12ba6-124">Developers should not use this interface.</span></span>

<span data-ttu-id="12ba6-125">O [**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) só está disponível no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="12ba6-125">[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) is only available on Windows Vista and later.</span></span>

<span data-ttu-id="12ba6-126">O código a seguir descreve como a interface **ITabletContextP** é definida.</span><span class="sxs-lookup"><span data-stu-id="12ba6-126">The following code describes how the **ITabletContextP** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a><span data-ttu-id="12ba6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12ba6-127">Requirements</span></span>



| <span data-ttu-id="12ba6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="12ba6-128">Requirement</span></span> | <span data-ttu-id="12ba6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="12ba6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12ba6-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12ba6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="12ba6-131">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="12ba6-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="12ba6-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12ba6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="12ba6-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="12ba6-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="12ba6-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12ba6-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="12ba6-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12ba6-135"><dt>Wisptis.exe</dt></span></span> </dl> |



 

