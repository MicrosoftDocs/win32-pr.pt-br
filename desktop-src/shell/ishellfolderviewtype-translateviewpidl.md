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
ms.openlocfilehash: 75876e5088c610c1f9f02ba9374db5cea4a6023c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502075"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a><span data-ttu-id="2cd4c-103">Método IShellFolderViewType:: TranslateViewPidl</span><span class="sxs-lookup"><span data-stu-id="2cd4c-103">IShellFolderViewType::TranslateViewPidl method</span></span>

<span data-ttu-id="2cd4c-104">Reconstrói um ponteiro para uma PIDL (lista de identificadores de item) de uma representação hierárquica da pasta do Shell em uma representação diferente.</span><span class="sxs-lookup"><span data-stu-id="2cd4c-104">Reconstructs a pointer to an item identifier list (PIDL) from one hierarchical representation of the Shell folder into a different representation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cd4c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cd4c-105">Syntax</span></span>


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="2cd4c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cd4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cd4c-107">*PIDL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2cd4c-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd4c-108">Tipo: **PCUIDLIST \_ relativo**</span><span class="sxs-lookup"><span data-stu-id="2cd4c-108">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="2cd4c-109">A matriz de IDs de item relativa à pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="2cd4c-109">The array of item IDs relative to the root folder.</span></span>

</dd> <dt>

<span data-ttu-id="2cd4c-110">*pidlView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2cd4c-110">*pidlView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd4c-111">Tipo: **PCUIDLIST \_ relativo**</span><span class="sxs-lookup"><span data-stu-id="2cd4c-111">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="2cd4c-112">PIDL especial da exibição.</span><span class="sxs-lookup"><span data-stu-id="2cd4c-112">Special PIDL of the view.</span></span>

</dd> <dt>

<span data-ttu-id="2cd4c-113">*ppidlOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2cd4c-113">*ppidlOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd4c-114">Tipo: \**PCUIDLIST \_ Relative \** _</span><span class="sxs-lookup"><span data-stu-id="2cd4c-114">Type: \**PCUIDLIST\_RELATIVE\** _</span></span>

<span data-ttu-id="2cd4c-115">O endereço de uma variável PIDL para receber a tradução.</span><span class="sxs-lookup"><span data-stu-id="2cd4c-115">The address of a PIDL variable to receive the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cd4c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2cd4c-116">Return value</span></span>

<span data-ttu-id="2cd4c-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2cd4c-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2cd4c-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2cd4c-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2cd4c-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2cd4c-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cd4c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cd4c-120">Remarks</span></span>

<span data-ttu-id="2cd4c-121">Quando terminar, você deverá liberar o PIDL retornado com [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span><span class="sxs-lookup"><span data-stu-id="2cd4c-121">When finished, you should free the returned PIDL with [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="2cd4c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cd4c-122">Requirements</span></span>



| <span data-ttu-id="2cd4c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cd4c-123">Requirement</span></span> | <span data-ttu-id="2cd4c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2cd4c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd4c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2cd4c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2cd4c-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2cd4c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2cd4c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2cd4c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2cd4c-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2cd4c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2cd4c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2cd4c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cd4c-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cd4c-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




