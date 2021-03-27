---
description: Inicia uma pesquisa para uma cadeia de caracteres de pesquisa especificada.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'Método IShellFolderSearchable:: FindString (MMC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647540"
---
# <a name="ishellfoldersearchablefindstring-method"></a><span data-ttu-id="3a985-103">Método IShellFolderSearchable:: FindString</span><span class="sxs-lookup"><span data-stu-id="3a985-103">IShellFolderSearchable::FindString method</span></span>

<span data-ttu-id="3a985-104">Inicia uma pesquisa para uma cadeia de caracteres de pesquisa especificada.</span><span class="sxs-lookup"><span data-stu-id="3a985-104">Begins a search for a specified search string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a985-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a985-105">Syntax</span></span>


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="3a985-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a985-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a985-107">*pwszTarget* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a985-107">*pwszTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a985-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3a985-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="3a985-109">Um ponteiro para uma cadeia de caracteres que especifica a palavra-chave Search.</span><span class="sxs-lookup"><span data-stu-id="3a985-109">A pointer to a string that specifies the search keyword.</span></span>

</dd> <dt>

<span data-ttu-id="3a985-110">*pdwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a985-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a985-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="3a985-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="3a985-112">Nenhum sinalizador está definido no momento; Defina como _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="3a985-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="3a985-113">*punkOnAsyncSearch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a985-113">*punkOnAsyncSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a985-114">Tipo: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="3a985-114">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="3a985-115">Um ponteiro para um objeto do tipo [_ *IUnknown* \*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="3a985-115">A pointer to an object of type [_ *IUnknown*\*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="3a985-116">Este objeto deve dar suporte à interface [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="3a985-116">This object must support the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface.</span></span> <span data-ttu-id="3a985-117">Defina como **NULL** se nenhum retorno de chamada for necessário.</span><span class="sxs-lookup"><span data-stu-id="3a985-117">Set to **NULL** if no callback is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="3a985-118">*ppidlOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3a985-118">*ppidlOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a985-119">Tipo: **LPITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="3a985-119">Type: **LPITEMIDLIST**</span></span>

<span data-ttu-id="3a985-120">Um ponteiro para uma estrutura de [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) para a pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3a985-120">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a985-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a985-121">Return value</span></span>

<span data-ttu-id="3a985-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3a985-122">Type: **HRESULT**</span></span>

<span data-ttu-id="3a985-123">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3a985-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3a985-124">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a985-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a985-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a985-125">Requirements</span></span>



| <span data-ttu-id="3a985-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a985-126">Requirement</span></span> | <span data-ttu-id="3a985-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3a985-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a985-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a985-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3a985-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a985-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3a985-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a985-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3a985-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a985-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3a985-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3a985-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a985-133"><dt>MMC. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a985-133"><dt>Mmc.h</dt></span></span> </dl>       |
| <span data-ttu-id="3a985-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3a985-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a985-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a985-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
