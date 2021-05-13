---
description: Recupera um enumerador que retornará um ponteiro para uma PIDL (lista de identificadores de item) para cada exibição estendida.
title: Método IShellFolderViewType::EnumViews
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 1627bb134066821444788ca44a3527278a02f4c7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842767"
---
# <a name="ishellfolderviewtypeenumviews-method"></a><span data-ttu-id="16f0c-103">Método IShellFolderViewType::EnumViews</span><span class="sxs-lookup"><span data-stu-id="16f0c-103">IShellFolderViewType::EnumViews method</span></span>

<span data-ttu-id="16f0c-104">Recupera um enumerador que retornará um ponteiro para uma PIDL (lista de identificadores de item) para cada exibição estendida.</span><span class="sxs-lookup"><span data-stu-id="16f0c-104">Retrieves an enumerator that will return one pointer to an item identifier list (PIDL) for every extended view.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f0c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16f0c-105">Syntax</span></span>


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="16f0c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16f0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16f0c-107">*grfFlags* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="16f0c-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16f0c-108">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="16f0c-108">Type: **ULONG**</span></span>

<span data-ttu-id="16f0c-109">Sinalizadores que indicam quais itens incluir na enumeração.</span><span class="sxs-lookup"><span data-stu-id="16f0c-109">Flags indicating which items to include in the enumeration.</span></span> <span data-ttu-id="16f0c-110">Para ver uma lista de valores possíveis, consulte o tipo enumerado [**SHCONTF.**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf)</span><span class="sxs-lookup"><span data-stu-id="16f0c-110">For a list of possible values, see the [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) enumerated type.</span></span> <span data-ttu-id="16f0c-111">Esse parâmetro pode ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="16f0c-111">This parameter may be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="16f0c-112">*ppenum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="16f0c-112">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16f0c-113">Tipo: **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span><span class="sxs-lookup"><span data-stu-id="16f0c-113">Type: **[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***</span></span>

<span data-ttu-id="16f0c-114">O endereço de uma variável de ponteiro do [**tipo IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) que recebe o enumerador.</span><span class="sxs-lookup"><span data-stu-id="16f0c-114">The address of a pointer variable of type [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) that receives the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16f0c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16f0c-115">Return value</span></span>

<span data-ttu-id="16f0c-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="16f0c-116">Type: **HRESULT**</span></span>

<span data-ttu-id="16f0c-117">Se esse método for bem-sucedido, ele **retornará S \_ OK.**</span><span class="sxs-lookup"><span data-stu-id="16f0c-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="16f0c-118">Caso contrário, ele retornará um **código de erro HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="16f0c-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="16f0c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="16f0c-119">Remarks</span></span>

<span data-ttu-id="16f0c-120">As exibições são representadas para o usuário como pastas ocultas fora do diretório raiz (representadas por PIDLs).</span><span class="sxs-lookup"><span data-stu-id="16f0c-120">Views are represented to the user as hidden folders off the root directory (represented by PIDLs).</span></span> <span data-ttu-id="16f0c-121">Sempre que apropriado, a exibição padrão (fora da pasta raiz) é representada como **NULL** ou vazio, PIDL.</span><span class="sxs-lookup"><span data-stu-id="16f0c-121">Whenever appropriate, the default view (off the root folder) is represented as the **NULL**, or empty, PIDL.</span></span>

## <a name="requirements"></a><span data-ttu-id="16f0c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16f0c-122">Requirements</span></span>



| <span data-ttu-id="16f0c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="16f0c-123">Requirement</span></span> | <span data-ttu-id="16f0c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="16f0c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16f0c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16f0c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="16f0c-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="16f0c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="16f0c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16f0c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="16f0c-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="16f0c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="16f0c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="16f0c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16f0c-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16f0c-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




