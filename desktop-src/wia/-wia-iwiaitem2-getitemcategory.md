---
description: Obtém as informações de categoria de um item.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'Método IWiaItem2:: GetItemCategory (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771375"
---
# <a name="iwiaitem2getitemcategory-method"></a><span data-ttu-id="ff3ec-103">Método IWiaItem2:: GetItemCategory</span><span class="sxs-lookup"><span data-stu-id="ff3ec-103">IWiaItem2::GetItemCategory method</span></span>

<span data-ttu-id="ff3ec-104">Obtém as informações de categoria de um item.</span><span class="sxs-lookup"><span data-stu-id="ff3ec-104">Gets an item's category information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff3ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff3ec-105">Syntax</span></span>


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a><span data-ttu-id="ff3ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff3ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff3ec-107">*pItemCategoryGUID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ff3ec-107">*pItemCategoryGUID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff3ec-108">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="ff3ec-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="ff3ec-109">Recebe um ponteiro para o GUID que identifica a categoria do item.</span><span class="sxs-lookup"><span data-stu-id="ff3ec-109">Receives a pointer to the GUID that identifies the category of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff3ec-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff3ec-110">Return value</span></span>

<span data-ttu-id="ff3ec-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ff3ec-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ff3ec-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ff3ec-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ff3ec-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff3ec-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff3ec-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff3ec-114">Remarks</span></span>

<span data-ttu-id="ff3ec-115">Cada objeto [**IWiaItem2**](-wia-iwiaitem2.md) na árvore hierárquica de objetos associados a um dispositivo de hardware WIA (Windows Image Acquisition) 2,0 tem uma categoria específica.</span><span class="sxs-lookup"><span data-stu-id="ff3ec-115">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific category.</span></span> <span data-ttu-id="ff3ec-116">Esse método permite que os aplicativos identifiquem a categoria de qualquer item em uma árvore hierárquica de objetos de item em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ff3ec-116">This method enables applications to identify the category of any item in a hierarchical tree of item objects in a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff3ec-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff3ec-117">Requirements</span></span>



| <span data-ttu-id="ff3ec-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff3ec-118">Requirement</span></span> | <span data-ttu-id="ff3ec-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ff3ec-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3ec-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff3ec-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ff3ec-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff3ec-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ff3ec-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff3ec-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ff3ec-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff3ec-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ff3ec-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff3ec-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff3ec-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff3ec-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff3ec-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="ff3ec-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff3ec-127"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff3ec-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 




