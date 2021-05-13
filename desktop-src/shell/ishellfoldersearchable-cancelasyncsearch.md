---
description: Inicia o processo de cancelar uma pesquisa assíncrona pendente.
title: 'Método IShellFolderSearchable:: CancelAsyncSearch'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: 3146fea4f6c8d8547c8c86096b434cbaea5b5926
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842987"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a><span data-ttu-id="b33e8-103">Método IShellFolderSearchable:: CancelAsyncSearch</span><span class="sxs-lookup"><span data-stu-id="b33e8-103">IShellFolderSearchable::CancelAsyncSearch method</span></span>

<span data-ttu-id="b33e8-104">Inicia o processo de cancelar uma pesquisa assíncrona pendente.</span><span class="sxs-lookup"><span data-stu-id="b33e8-104">Begins the process of canceling a pending asynchronous search.</span></span>

## <a name="syntax"></a><span data-ttu-id="b33e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b33e8-105">Syntax</span></span>


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b33e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b33e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b33e8-107">*pidlSearch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b33e8-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b33e8-108">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="b33e8-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="b33e8-109">Um ponteiro para uma [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b33e8-109">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) for the search.</span></span>

</dd> <dt>

<span data-ttu-id="b33e8-110">*pdwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b33e8-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b33e8-111">Tipo: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="b33e8-111">Type: **DWORD\***</span></span>

<span data-ttu-id="b33e8-112">Nenhum sinalizador está definido no momento; Defina como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b33e8-112">No flags are currently defined; set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b33e8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b33e8-113">Return value</span></span>

<span data-ttu-id="b33e8-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b33e8-114">Type: **HRESULT**</span></span>

<span data-ttu-id="b33e8-115">Retorna S \_ OK se cancelar, ou S \_ false se a pesquisa não estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="b33e8-115">Returns S\_OK if canceling, or S\_FALSE if search is not running.</span></span>

## <a name="remarks"></a><span data-ttu-id="b33e8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b33e8-116">Remarks</span></span>

<span data-ttu-id="b33e8-117">Quando a pesquisa for realmente cancelada, [**RunEnd**](ishellfoldersearchablecallback-runend.md) será chamado.</span><span class="sxs-lookup"><span data-stu-id="b33e8-117">When the search is actually canceled, [**RunEnd**](ishellfoldersearchablecallback-runend.md) will be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="b33e8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b33e8-118">Requirements</span></span>



| <span data-ttu-id="b33e8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b33e8-119">Requirement</span></span> | <span data-ttu-id="b33e8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b33e8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b33e8-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b33e8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b33e8-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b33e8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b33e8-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b33e8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b33e8-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b33e8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b33e8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b33e8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b33e8-126"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b33e8-126"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




