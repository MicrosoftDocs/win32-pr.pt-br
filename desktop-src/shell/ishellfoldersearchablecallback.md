---
description: Expõe rotinas de retorno de chamada para monitorar o processo de pesquisa.
title: Interface IShellFolderSearchableCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3412a01b-d5ea-44e1-819c-f10f81fac391
ms.openlocfilehash: cf1a3b03eed2a15e82e1313875a4ab8584243190
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842777"
---
# <a name="ishellfoldersearchablecallback-interface"></a><span data-ttu-id="369a2-103">Interface IShellFolderSearchableCallback</span><span class="sxs-lookup"><span data-stu-id="369a2-103">IShellFolderSearchableCallback interface</span></span>

<span data-ttu-id="369a2-104">Expõe rotinas de retorno de chamada para monitorar o processo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="369a2-104">Exposes callback routines to monitor the search process.</span></span>

## <a name="members"></a><span data-ttu-id="369a2-105">Membros</span><span class="sxs-lookup"><span data-stu-id="369a2-105">Members</span></span>

<span data-ttu-id="369a2-106">A interface **IShellFolderSearchableCallback** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="369a2-106">The **IShellFolderSearchableCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="369a2-107">**IShellFolderSearchableCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="369a2-107">**IShellFolderSearchableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="369a2-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="369a2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="369a2-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="369a2-109">Methods</span></span>

<span data-ttu-id="369a2-110">A interface **IShellFolderSearchableCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="369a2-110">The **IShellFolderSearchableCallback** interface has these methods.</span></span>



| <span data-ttu-id="369a2-111">Método</span><span class="sxs-lookup"><span data-stu-id="369a2-111">Method</span></span>                                                      | <span data-ttu-id="369a2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="369a2-112">Description</span></span>                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="369a2-113">**RunBegin**</span><span class="sxs-lookup"><span data-stu-id="369a2-113">**RunBegin**</span></span>](ishellfoldersearchablecallback-runbegin.md) | <span data-ttu-id="369a2-114">Indica que uma pesquisa foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="369a2-114">Indicates that a search was started.</span></span><br/>  |
| [<span data-ttu-id="369a2-115">**RunEnd**</span><span class="sxs-lookup"><span data-stu-id="369a2-115">**RunEnd**</span></span>](ishellfoldersearchablecallback-runend.md)     | <span data-ttu-id="369a2-116">Indica que uma pesquisa foi concluída.</span><span class="sxs-lookup"><span data-stu-id="369a2-116">Indicates that a search has finished.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="369a2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="369a2-117">Remarks</span></span>

<span data-ttu-id="369a2-118">Essa interface não está definida em nenhum arquivo de header público.</span><span class="sxs-lookup"><span data-stu-id="369a2-118">This interface is not defined in any public header files.</span></span> <span data-ttu-id="369a2-119">Se você optar por implementar essa interface, poderá usar o código C/C++ a seguir para declarar seus métodos.</span><span class="sxs-lookup"><span data-stu-id="369a2-119">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchableCallback Methods ***

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a><span data-ttu-id="369a2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="369a2-120">Requirements</span></span>



| <span data-ttu-id="369a2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="369a2-121">Requirement</span></span> | <span data-ttu-id="369a2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="369a2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="369a2-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="369a2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="369a2-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="369a2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="369a2-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="369a2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="369a2-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="369a2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="369a2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="369a2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="369a2-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="369a2-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
