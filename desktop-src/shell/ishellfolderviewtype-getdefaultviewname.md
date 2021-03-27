---
description: Obtém o nome da exibição padrão. Chame GetDisplayNameOf para recuperar os nomes das outras exibições.
title: 'Método IShellFolderViewType:: getmodopadrãoname'
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
ms.openlocfilehash: 239fcd80bcfc0b29287f8e16aeef3efb8ae032c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967497"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a><span data-ttu-id="68549-104">Método IShellFolderViewType:: getmodopadrãoname</span><span class="sxs-lookup"><span data-stu-id="68549-104">IShellFolderViewType::GetDefaultViewName method</span></span>

<span data-ttu-id="68549-105">Obtém o nome da exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="68549-105">Gets the name of the default view.</span></span> <span data-ttu-id="68549-106">Chame [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para recuperar os nomes das outras exibições.</span><span class="sxs-lookup"><span data-stu-id="68549-106">Call [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span>

## <a name="syntax"></a><span data-ttu-id="68549-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68549-107">Syntax</span></span>


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="68549-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68549-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68549-109">*uFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68549-109">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68549-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="68549-110">Type: **DWORD**</span></span>

<span data-ttu-id="68549-111">Sinalizadores opcionais; deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="68549-111">Optional flags; should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="68549-112">*ppwszName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="68549-112">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68549-113">Tipo: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="68549-113">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="68549-114">O endereço de um ponteiro de cadeia de caracteres que recebe o nome de exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="68549-114">The address of a string pointer that receives the default view name.</span></span> <span data-ttu-id="68549-115">A memória da cadeia de caracteres é alocada com [_ *SHStrDup* \*](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span><span class="sxs-lookup"><span data-stu-id="68549-115">The memory for the string is allocated with [_ *SHStrDup*\*](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68549-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68549-116">Return value</span></span>

<span data-ttu-id="68549-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="68549-117">Type: **HRESULT**</span></span>

<span data-ttu-id="68549-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="68549-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68549-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68549-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="68549-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68549-120">Requirements</span></span>



| <span data-ttu-id="68549-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="68549-121">Requirement</span></span> | <span data-ttu-id="68549-122">Valor</span><span class="sxs-lookup"><span data-stu-id="68549-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68549-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68549-123">Minimum supported client</span></span><br/> | <span data-ttu-id="68549-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="68549-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="68549-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68549-125">Minimum supported server</span></span><br/> | <span data-ttu-id="68549-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="68549-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="68549-127">DLL</span><span class="sxs-lookup"><span data-stu-id="68549-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68549-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68549-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




