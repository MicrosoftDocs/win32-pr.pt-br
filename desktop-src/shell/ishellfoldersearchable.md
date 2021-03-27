---
description: Expõe métodos que permitem que uma extensão de shell forneça um namespace pesquisável.
title: Interface IShellFolderSearchable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 359def5c-d7ad-46bd-bdda-30a7b3eea56c
ms.openlocfilehash: 1f42b3af012361bfd24c93e03c38e6954eb5326e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967498"
---
# <a name="ishellfoldersearchable-interface"></a><span data-ttu-id="6f4c6-103">Interface IShellFolderSearchable</span><span class="sxs-lookup"><span data-stu-id="6f4c6-103">IShellFolderSearchable interface</span></span>

<span data-ttu-id="6f4c6-104">Expõe métodos que permitem que uma extensão de shell forneça um namespace pesquisável.</span><span class="sxs-lookup"><span data-stu-id="6f4c6-104">Exposes methods that allow a Shell extension to provide a searchable namespace.</span></span>

## <a name="members"></a><span data-ttu-id="6f4c6-105">Membros</span><span class="sxs-lookup"><span data-stu-id="6f4c6-105">Members</span></span>

<span data-ttu-id="6f4c6-106">A interface **IShellFolderSearchable** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6f4c6-106">The **IShellFolderSearchable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6f4c6-107">**IShellFolderSearchable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6f4c6-107">**IShellFolderSearchable** also has these types of members:</span></span>

-   [<span data-ttu-id="6f4c6-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6f4c6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6f4c6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6f4c6-109">Methods</span></span>

<span data-ttu-id="6f4c6-110">A interface **IShellFolderSearchable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6f4c6-110">The **IShellFolderSearchable** interface has these methods.</span></span>



| <span data-ttu-id="6f4c6-111">Método</span><span class="sxs-lookup"><span data-stu-id="6f4c6-111">Method</span></span>                                                                | <span data-ttu-id="6f4c6-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f4c6-112">Description</span></span>                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="6f4c6-113">**CancelAsyncSearch**</span><span class="sxs-lookup"><span data-stu-id="6f4c6-113">**CancelAsyncSearch**</span></span>](ishellfoldersearchable-cancelasyncsearch.md) | <span data-ttu-id="6f4c6-114">Inicia o processo de cancelar uma pesquisa assíncrona pendente.</span><span class="sxs-lookup"><span data-stu-id="6f4c6-114">Begins the process of canceling a pending asynchronous search.</span></span><br/> |
| [<span data-ttu-id="6f4c6-115">**FindString**</span><span class="sxs-lookup"><span data-stu-id="6f4c6-115">**FindString**</span></span>](ishellfoldersearchable-findstring.md)               | <span data-ttu-id="6f4c6-116">Inicia uma pesquisa para uma cadeia de caracteres de pesquisa especificada.</span><span class="sxs-lookup"><span data-stu-id="6f4c6-116">Begins a search for a specified search string.</span></span><br/>                 |
| [<span data-ttu-id="6f4c6-117">**InvalidateSearch**</span><span class="sxs-lookup"><span data-stu-id="6f4c6-117">**InvalidateSearch**</span></span>](ishellfoldersearchable-invalidatesearch.md)   | <span data-ttu-id="6f4c6-118">Torna esse PIDL uma parte inválida da pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="6f4c6-118">Makes this PIDL an invalid portion of the Shell folder.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="6f4c6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f4c6-119">Remarks</span></span>

<span data-ttu-id="6f4c6-120">Essa interface não está definida em nenhum arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="6f4c6-120">This interface is not defined in any public header files.</span></span> <span data-ttu-id="6f4c6-121">Se você optar por implementar essa interface, poderá usar o código C/C++ a seguir para declarar seus métodos.</span><span class="sxs-lookup"><span data-stu-id="6f4c6-121">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchable
DECLARE_INTERFACE_IID_(IShellFolderSearchable, IUnknown, "4E1AE66C-204B-11d2-8DB3-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderSearchable methods _*_

    // FindString -
    //  The returned Shell folder's enumerator will have any
    //   search hits for the given search string.
    //  punkOnAsyncSearch will be QI'd for IShellFolderSearchableCallback
    STDMETHOD(FindString)(THIS_ LPCWSTR pwszTarget, __inout_opt DWORD _pdwFlags,
                          __in_opt IUnknown *punkOnAsyncSearch, __out LPITEMIDLIST *ppidlOut)   PURE;
    // CancelAsyncSearch -
    //   Begins the process of canceling any pending
    //    asynchronous search from this pidl.
    //    When the search is actually canceled, RunEnd will be called
    //   Returns: S_OK => cancelling, S_FALSE => not running
    STDMETHOD(CancelAsyncSearch) (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;

    // InvalidateSearch -
    //   Makes this pidl no longer a valid portion of the Shell folder
    //    Also does some cleanup of any databases used in the search and
    //    will cause the eventual release of the callback
    //   May cause async search to be canceled
    STDMETHOD(InvalidateSearch)  (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;
};
```



## <a name="requirements"></a><span data-ttu-id="6f4c6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f4c6-122">Requirements</span></span>



| <span data-ttu-id="6f4c6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f4c6-123">Requirement</span></span> | <span data-ttu-id="6f4c6-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6f4c6-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4c6-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f4c6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6f4c6-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f4c6-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6f4c6-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f4c6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6f4c6-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f4c6-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6f4c6-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6f4c6-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f4c6-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f4c6-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
