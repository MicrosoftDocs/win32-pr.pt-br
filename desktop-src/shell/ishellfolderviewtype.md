---
description: Expõe métodos que habilitam uma pasta shell para dar suporte a diferentes exibições em seu conteúdo (layouts hierárquicos diferentes de seus dados).
title: Interface IShellFolderViewType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9b597f6b-ef27-4fa1-ad00-e131dbd979e7
ms.openlocfilehash: f3ccb4073d59e0ebe9b840bd6f8f592f463e1e46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842687"
---
# <a name="ishellfolderviewtype-interface"></a><span data-ttu-id="15a38-103">Interface IShellFolderViewType</span><span class="sxs-lookup"><span data-stu-id="15a38-103">IShellFolderViewType interface</span></span>

<span data-ttu-id="15a38-104">Expõe métodos que habilitam uma pasta shell para dar suporte a diferentes exibições em seu conteúdo (layouts hierárquicos diferentes de seus dados).</span><span class="sxs-lookup"><span data-stu-id="15a38-104">Exposes methods that enable a Shell folder to support different views on its content (different hierarchical layouts of its data).</span></span>

## <a name="members"></a><span data-ttu-id="15a38-105">Membros</span><span class="sxs-lookup"><span data-stu-id="15a38-105">Members</span></span>

<span data-ttu-id="15a38-106">A interface **IShellFolderViewType** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="15a38-106">The **IShellFolderViewType** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="15a38-107">**IShellFolderViewType** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="15a38-107">**IShellFolderViewType** also has these types of members:</span></span>

-   [<span data-ttu-id="15a38-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="15a38-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="15a38-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="15a38-109">Methods</span></span>

<span data-ttu-id="15a38-110">A interface **IShellFolderViewType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="15a38-110">The **IShellFolderViewType** interface has these methods.</span></span>



| <span data-ttu-id="15a38-111">Método</span><span class="sxs-lookup"><span data-stu-id="15a38-111">Method</span></span>                                                                      | <span data-ttu-id="15a38-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="15a38-112">Description</span></span>                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15a38-113">**EnumViews**</span><span class="sxs-lookup"><span data-stu-id="15a38-113">**EnumViews**</span></span>](ishellfolderviewtype-enumviews.md)                         | <span data-ttu-id="15a38-114">Recupera um enumerador que retornará um PIDL para cada exibição estendida.</span><span class="sxs-lookup"><span data-stu-id="15a38-114">Retrieves an enumerator that will return one PIDL for every extended view.</span></span><br/>                                                                                |
| [<span data-ttu-id="15a38-115">**GetDefaultViewName**</span><span class="sxs-lookup"><span data-stu-id="15a38-115">**GetDefaultViewName**</span></span>](ishellfolderviewtype-getdefaultviewname.md)       | <span data-ttu-id="15a38-116">Obtém o nome da exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="15a38-116">Gets the name of the default view.</span></span> <span data-ttu-id="15a38-117">Chame [**IShellFolder::GetDisplayNameOf para**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) recuperar os nomes das outras exibições.</span><span class="sxs-lookup"><span data-stu-id="15a38-117">Call [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span><br/> |
| [<span data-ttu-id="15a38-118">**GetViewTypeProperties**</span><span class="sxs-lookup"><span data-stu-id="15a38-118">**GetViewTypeProperties**</span></span>](ishellfolderviewtype-getviewtypeproperties.md) | <span data-ttu-id="15a38-119">Obtém as propriedades da exibição.</span><span class="sxs-lookup"><span data-stu-id="15a38-119">Gets the properties of the view.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="15a38-120">**TranslateViewPidl**</span><span class="sxs-lookup"><span data-stu-id="15a38-120">**TranslateViewPidl**</span></span>](ishellfolderviewtype-translateviewpidl.md)         | <span data-ttu-id="15a38-121">Reconstrói um PIDL de uma representação hierárquica da pasta Shell em uma representação diferente.</span><span class="sxs-lookup"><span data-stu-id="15a38-121">Reconstructs a PIDL from one hierarchical representation of the Shell folder into a different representation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="15a38-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="15a38-122">Remarks</span></span>

<span data-ttu-id="15a38-123">Esse enumerador retorna PIDLs que são pastas ocultas especiais no nível superior da pasta Shell, que não são enumeradas de outra forma.</span><span class="sxs-lookup"><span data-stu-id="15a38-123">This enumerator returns PIDLs that are special hidden folders at the top level of the Shell folder, which are not otherwise enumerated.</span></span> <span data-ttu-id="15a38-124">A exibição padrão é aquela que a pasta Shell exibe normalmente.</span><span class="sxs-lookup"><span data-stu-id="15a38-124">The default view is the one the Shell folder displays normally.</span></span>

<span data-ttu-id="15a38-125">Essa interface não está definida em nenhum arquivo de header público.</span><span class="sxs-lookup"><span data-stu-id="15a38-125">This interface is not defined in any public header file.</span></span> <span data-ttu-id="15a38-126">Se você optar por implementar essa interface, poderá usar o código C/C++ a seguir para declarar seus métodos.</span><span class="sxs-lookup"><span data-stu-id="15a38-126">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderViewType Methods ***

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList **ppenum) PURE;

    // GetDefaultViewName:
    //   Returns the name of the default view.  The names of the other views
    //   can be retrieved by calling GetDisplayNameOf.
    STDMETHOD(GetDefaultViewName)(THIS_ DWORD  uFlags, __out LPWSTR *ppwszName) PURE;
    STDMETHOD(GetViewTypeProperties)(THIS_ PCUITEMID_CHILD pidl, __out DWORD *pdwFlags)  PURE;

    // TranslateViewPidl:
    //   Attempts to take a pidl represented in one hierarchical representation of
    //   the Shell folder, and find it in a different representation.
    //   pidl should be relative to the root folder.
    //   Remember to ILFree ppidlOut
    STDMETHOD(TranslateViewPidl)(THIS_ PCUIDLIST_RELATIVE pidl, PCUIDLIST_RELATIVE pidlView,
              __out PIDLIST_RELATIVE *ppidlOut) PURE;
};

#define SFVTFLAG_NOTIFY_CREATE  0x00000001
#define SFVTFLAG_NOTIFY_RESORT  0x00000002
```



## <a name="requirements"></a><span data-ttu-id="15a38-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15a38-127">Requirements</span></span>



| <span data-ttu-id="15a38-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="15a38-128">Requirement</span></span> | <span data-ttu-id="15a38-129">Valor</span><span class="sxs-lookup"><span data-stu-id="15a38-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15a38-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15a38-130">Minimum supported client</span></span><br/> | <span data-ttu-id="15a38-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15a38-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="15a38-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15a38-132">Minimum supported server</span></span><br/> | <span data-ttu-id="15a38-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15a38-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="15a38-134">DLL</span><span class="sxs-lookup"><span data-stu-id="15a38-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15a38-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15a38-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
