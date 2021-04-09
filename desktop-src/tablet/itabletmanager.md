---
description: Fornece acesso a todos os tablets conectados ao computador.
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: Interface ITabletManager
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3400d98a832819d1edd640cd78586f1cfb06bdee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011774"
---
# <a name="itabletmanager-interface"></a><span data-ttu-id="9486f-103">Interface ITabletManager</span><span class="sxs-lookup"><span data-stu-id="9486f-103">ITabletManager interface</span></span>

<span data-ttu-id="9486f-104">Fornece acesso a todos os tablets conectados ao computador.</span><span class="sxs-lookup"><span data-stu-id="9486f-104">Provides access to all of the tablets attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="9486f-105">Membros</span><span class="sxs-lookup"><span data-stu-id="9486f-105">Members</span></span>

<span data-ttu-id="9486f-106">A interface **ITabletManager** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9486f-106">The **ITabletManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9486f-107">**ITabletManager** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9486f-107">**ITabletManager** also has these types of members:</span></span>

-   [<span data-ttu-id="9486f-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="9486f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9486f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9486f-109">Methods</span></span>

<span data-ttu-id="9486f-110">A interface **ITabletManager** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9486f-110">The **ITabletManager** interface has these methods.</span></span>



| <span data-ttu-id="9486f-111">Método</span><span class="sxs-lookup"><span data-stu-id="9486f-111">Method</span></span>                                                  | <span data-ttu-id="9486f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9486f-112">Description</span></span>                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| <span data-ttu-id="9486f-113">[**GetTableName**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9486f-113">[**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span></span>           | <span data-ttu-id="9486f-114">Recupera o objeto do Tablet especificado.</span><span class="sxs-lookup"><span data-stu-id="9486f-114">Retrieves the specified tablet object.</span></span><br/>                  |
| [<span data-ttu-id="9486f-115">**GetTabletCount**</span><span class="sxs-lookup"><span data-stu-id="9486f-115">**GetTabletCount**</span></span>](itabletmanager-gettabletcount.md) | <span data-ttu-id="9486f-116">Recupera o número de tablets anexados ao sistema.</span><span class="sxs-lookup"><span data-stu-id="9486f-116">Retrieves the number of tablets attached to the system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9486f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9486f-117">Remarks</span></span>

<span data-ttu-id="9486f-118">Os desenvolvedores não devem usar essa interface.</span><span class="sxs-lookup"><span data-stu-id="9486f-118">Developers should not use this interface.</span></span>

<span data-ttu-id="9486f-119">O código a seguir mostra como a interface **ITabletManager** é implementada.</span><span class="sxs-lookup"><span data-stu-id="9486f-119">The following code shows how the **ITabletManager** interface is implemented.</span></span>

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

<span data-ttu-id="9486f-120">Chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com uma ID de classe de CLSID \_ TabletManagerS e, em seguida, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um ponteiro para a **interface ITabletManager**.</span><span class="sxs-lookup"><span data-stu-id="9486f-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class ID of CLSID\_TabletManagerS, and then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the **ITabletManager Interface**.</span></span> <span data-ttu-id="9486f-121">O \_ GUID TabletManagerS do CLSID é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9486f-121">The CLSID\_TabletManagerS GUID is defined as follows:</span></span>

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a><span data-ttu-id="9486f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9486f-122">Requirements</span></span>



| <span data-ttu-id="9486f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9486f-123">Requirement</span></span> | <span data-ttu-id="9486f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9486f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9486f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9486f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9486f-126">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9486f-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9486f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9486f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9486f-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9486f-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9486f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9486f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="9486f-130"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9486f-130"><dt>Wisptis.exe</dt></span></span> </dl> |



 

