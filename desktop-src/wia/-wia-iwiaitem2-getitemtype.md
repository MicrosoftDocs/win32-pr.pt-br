---
description: Obtém as informações de tipo de um item.
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'Método IWiaItem2:: GetItemType (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647220"
---
# <a name="iwiaitem2getitemtype-method"></a><span data-ttu-id="5efe6-103">Método IWiaItem2:: GetItemType</span><span class="sxs-lookup"><span data-stu-id="5efe6-103">IWiaItem2::GetItemType method</span></span>

<span data-ttu-id="5efe6-104">Obtém as informações de tipo de um item.</span><span class="sxs-lookup"><span data-stu-id="5efe6-104">Gets an item's type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5efe6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5efe6-105">Syntax</span></span>


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a><span data-ttu-id="5efe6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5efe6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5efe6-107">*pItemType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5efe6-107">*pItemType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5efe6-108">Tipo: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="5efe6-108">Type: \**LONG\** _</span></span>

<span data-ttu-id="5efe6-109">Recebe um ponteiro para um _ *Long*\* que contém uma combinação de sinalizadores de tipo.</span><span class="sxs-lookup"><span data-stu-id="5efe6-109">Receives a pointer to a _ *LONG*\* that contains a combination of type flags.</span></span> <span data-ttu-id="5efe6-110">Consulte [**sinalizadores de tipo de item WIA**](-wia-wia-item-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5efe6-110">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5efe6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5efe6-111">Return value</span></span>

<span data-ttu-id="5efe6-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5efe6-112">Type: **HRESULT**</span></span>

<span data-ttu-id="5efe6-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5efe6-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5efe6-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5efe6-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5efe6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5efe6-115">Remarks</span></span>

<span data-ttu-id="5efe6-116">Cada objeto [**IWiaItem2**](-wia-iwiaitem2.md) na árvore hierárquica de objetos associados a um dispositivo de hardware de aquisição de imagem do Windows (WIA) 2,0 tem um tipo de dados específico.</span><span class="sxs-lookup"><span data-stu-id="5efe6-116">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific data type.</span></span> <span data-ttu-id="5efe6-117">Os objetos de item representam pastas e arquivos.</span><span class="sxs-lookup"><span data-stu-id="5efe6-117">Item objects represent folders and files.</span></span> <span data-ttu-id="5efe6-118">As pastas contêm objetos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5efe6-118">Folders contain file objects.</span></span> <span data-ttu-id="5efe6-119">Os objetos de arquivo contêm dados adquiridos pelo dispositivo, como imagens e sons.</span><span class="sxs-lookup"><span data-stu-id="5efe6-119">File objects contain data acquired by the device such as images and sounds.</span></span> <span data-ttu-id="5efe6-120">Esse método permite que os aplicativos identifiquem o tipo de qualquer item em uma árvore hierárquica de objetos de item em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5efe6-120">This method enables applications to identify the type of any item in a hierarchical tree of item objects in a device.</span></span>

<span data-ttu-id="5efe6-121">Um item pode ter mais de um tipo.</span><span class="sxs-lookup"><span data-stu-id="5efe6-121">An item may have more than one type.</span></span> <span data-ttu-id="5efe6-122">Por exemplo, um item que representa um arquivo de áudio terá os atributos de tipo [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.</span><span class="sxs-lookup"><span data-stu-id="5efe6-122">For example, an item that represents an audio file will have the type attributes [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5efe6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5efe6-123">Requirements</span></span>



| <span data-ttu-id="5efe6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5efe6-124">Requirement</span></span> | <span data-ttu-id="5efe6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5efe6-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5efe6-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5efe6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5efe6-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5efe6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5efe6-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5efe6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5efe6-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5efe6-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5efe6-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5efe6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5efe6-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5efe6-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="5efe6-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="5efe6-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5efe6-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5efe6-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 




