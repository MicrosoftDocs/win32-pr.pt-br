---
description: Reconstrói um ponteiro para uma PIDL (lista de identificadores de item) de uma representação hierárquica da pasta do Shell em uma representação diferente.
title: 'Método IShellFolderViewType:: TranslateViewPidl'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 537a77e7ffffb462e0031ea0959f60cd695f7d99
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842667"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a><span data-ttu-id="60a4a-103">Método IShellFolderViewType:: TranslateViewPidl</span><span class="sxs-lookup"><span data-stu-id="60a4a-103">IShellFolderViewType::TranslateViewPidl method</span></span>

<span data-ttu-id="60a4a-104">Reconstrói um ponteiro para uma PIDL (lista de identificadores de item) de uma representação hierárquica da pasta do Shell em uma representação diferente.</span><span class="sxs-lookup"><span data-stu-id="60a4a-104">Reconstructs a pointer to an item identifier list (PIDL) from one hierarchical representation of the Shell folder into a different representation.</span></span>

## <a name="syntax"></a><span data-ttu-id="60a4a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60a4a-105">Syntax</span></span>


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="60a4a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60a4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60a4a-107">*PIDL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60a4a-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60a4a-108">Tipo: **PCUIDLIST \_ relativo**</span><span class="sxs-lookup"><span data-stu-id="60a4a-108">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="60a4a-109">A matriz de IDs de item relativa à pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="60a4a-109">The array of item IDs relative to the root folder.</span></span>

</dd> <dt>

<span data-ttu-id="60a4a-110">*pidlView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60a4a-110">*pidlView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60a4a-111">Tipo: **PCUIDLIST \_ relativo**</span><span class="sxs-lookup"><span data-stu-id="60a4a-111">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="60a4a-112">PIDL especial da exibição.</span><span class="sxs-lookup"><span data-stu-id="60a4a-112">Special PIDL of the view.</span></span>

</dd> <dt>

<span data-ttu-id="60a4a-113">*ppidlOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60a4a-113">*ppidlOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60a4a-114">Tipo: **PCUIDLIST \_ relativo \***</span><span class="sxs-lookup"><span data-stu-id="60a4a-114">Type: **PCUIDLIST\_RELATIVE\***</span></span>

<span data-ttu-id="60a4a-115">O endereço de uma variável PIDL para receber a tradução.</span><span class="sxs-lookup"><span data-stu-id="60a4a-115">The address of a PIDL variable to receive the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60a4a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="60a4a-116">Return value</span></span>

<span data-ttu-id="60a4a-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="60a4a-117">Type: **HRESULT**</span></span>

<span data-ttu-id="60a4a-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="60a4a-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="60a4a-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="60a4a-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="60a4a-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="60a4a-120">Remarks</span></span>

<span data-ttu-id="60a4a-121">Quando terminar, você deverá liberar o PIDL retornado com [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span><span class="sxs-lookup"><span data-stu-id="60a4a-121">When finished, you should free the returned PIDL with [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="60a4a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60a4a-122">Requirements</span></span>



| <span data-ttu-id="60a4a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="60a4a-123">Requirement</span></span> | <span data-ttu-id="60a4a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="60a4a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60a4a-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60a4a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="60a4a-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="60a4a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="60a4a-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60a4a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="60a4a-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="60a4a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="60a4a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="60a4a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60a4a-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60a4a-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




