---
description: Obtém o nome da exibição padrão. Chame GetDisplayNameOf para recuperar os nomes das outras exibições.
title: Método IShellFolderViewType::GetDefaultViewName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 808f68093512e2da602d5e73775b47943b140a46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842757"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a><span data-ttu-id="798ff-104">Método IShellFolderViewType::GetDefaultViewName</span><span class="sxs-lookup"><span data-stu-id="798ff-104">IShellFolderViewType::GetDefaultViewName method</span></span>

<span data-ttu-id="798ff-105">Obtém o nome da exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="798ff-105">Gets the name of the default view.</span></span> <span data-ttu-id="798ff-106">Chame [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para recuperar os nomes das outras exibições.</span><span class="sxs-lookup"><span data-stu-id="798ff-106">Call [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span>

## <a name="syntax"></a><span data-ttu-id="798ff-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="798ff-107">Syntax</span></span>


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="798ff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="798ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="798ff-109">*uFlags* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="798ff-109">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="798ff-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="798ff-110">Type: **DWORD**</span></span>

<span data-ttu-id="798ff-111">Sinalizadores opcionais; deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="798ff-111">Optional flags; should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="798ff-112">*ppwszName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="798ff-112">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="798ff-113">Tipo: **LPWSTR \***</span><span class="sxs-lookup"><span data-stu-id="798ff-113">Type: **LPWSTR\***</span></span>

<span data-ttu-id="798ff-114">O endereço de um ponteiro de cadeia de caracteres que recebe o nome de exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="798ff-114">The address of a string pointer that receives the default view name.</span></span> <span data-ttu-id="798ff-115">A memória da cadeia de caracteres é alocada com [**SHStrDup.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa)</span><span class="sxs-lookup"><span data-stu-id="798ff-115">The memory for the string is allocated with [**SHStrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="798ff-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="798ff-116">Return value</span></span>

<span data-ttu-id="798ff-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="798ff-117">Type: **HRESULT**</span></span>

<span data-ttu-id="798ff-118">Se esse método for bem-sucedido, ele **retornará S \_ OK.**</span><span class="sxs-lookup"><span data-stu-id="798ff-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="798ff-119">Caso contrário, ele retornará um **código de erro HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="798ff-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="798ff-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="798ff-120">Requirements</span></span>



| <span data-ttu-id="798ff-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="798ff-121">Requirement</span></span> | <span data-ttu-id="798ff-122">Valor</span><span class="sxs-lookup"><span data-stu-id="798ff-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="798ff-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="798ff-123">Minimum supported client</span></span><br/> | <span data-ttu-id="798ff-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="798ff-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="798ff-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="798ff-125">Minimum supported server</span></span><br/> | <span data-ttu-id="798ff-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="798ff-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="798ff-127">DLL</span><span class="sxs-lookup"><span data-stu-id="798ff-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="798ff-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="798ff-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




