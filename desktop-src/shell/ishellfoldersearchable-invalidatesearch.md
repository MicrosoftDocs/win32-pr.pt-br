---
description: Torna esse ponteiro para uma lista de identificadores de item (PIDL) uma parte inválida da pasta do Shell.
title: 'Método IShellFolderSearchable:: InvalidateSearch'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 43d76c6a27b301a61474b8028af16e5e540cf2ce
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841687"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a><span data-ttu-id="7ec51-103">Método IShellFolderSearchable:: InvalidateSearch</span><span class="sxs-lookup"><span data-stu-id="7ec51-103">IShellFolderSearchable::InvalidateSearch method</span></span>

<span data-ttu-id="7ec51-104">Torna esse ponteiro para uma lista de identificadores de item (PIDL) uma parte inválida da pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="7ec51-104">Makes this pointer to an item identifier list (PIDL) an invalid portion of the Shell folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec51-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ec51-105">Syntax</span></span>


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7ec51-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ec51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ec51-107">*pidlSearch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ec51-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec51-108">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="7ec51-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="7ec51-109">Um ponteiro para a estrutura de [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) da pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7ec51-109">A pointer to the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> <dt>

<span data-ttu-id="7ec51-110">*pdwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ec51-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ec51-111">Tipo: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="7ec51-111">Type: **DWORD\***</span></span>

<span data-ttu-id="7ec51-112">Nenhum sinalizador está definido no momento; Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7ec51-112">No flags are currently defined; set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ec51-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ec51-113">Return value</span></span>

<span data-ttu-id="7ec51-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7ec51-114">Type: **HRESULT**</span></span>

<span data-ttu-id="7ec51-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7ec51-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ec51-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ec51-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ec51-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ec51-117">Remarks</span></span>

<span data-ttu-id="7ec51-118">Quando uma pasta de pesquisa é invalidada, ela pode executar a limpeza de todos os recursos que ele usou.</span><span class="sxs-lookup"><span data-stu-id="7ec51-118">When a search folder is invalidated, it can perform cleanup of any resources it has used.</span></span> <span data-ttu-id="7ec51-119">O método **IShellFolderSearchable:: InvalidateSearch** pode fazer com que uma pesquisa assíncrona seja cancelada e resultará na versão eventual do objeto de interface [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="7ec51-119">The **IShellFolderSearchable::InvalidateSearch** method may cause an asynchronous search to be canceled and will result in the eventual release of the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec51-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ec51-120">Requirements</span></span>



| <span data-ttu-id="7ec51-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ec51-121">Requirement</span></span> | <span data-ttu-id="7ec51-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7ec51-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec51-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ec51-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec51-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7ec51-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7ec51-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ec51-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec51-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7ec51-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7ec51-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7ec51-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ec51-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ec51-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




