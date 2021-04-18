---
description: Remove o objeto IWiaItem2 atual da árvore de objetos do dispositivo.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: 'IWiaItem2: método eleteItem de:D (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ef6a4204b591f06811f0941ca0ceed72b76151db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793855"
---
# <a name="iwiaitem2deleteitem-method"></a><span data-ttu-id="41951-103">IWiaItem2: método eleteItem de:D</span><span class="sxs-lookup"><span data-stu-id="41951-103">IWiaItem2::DeleteItem method</span></span>

<span data-ttu-id="41951-104">Remove o objeto [**IWiaItem2**](-wia-iwiaitem2.md) atual da árvore de objetos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41951-104">Removes the current [**IWiaItem2**](-wia-iwiaitem2.md) object from the device's object tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="41951-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41951-105">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="41951-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41951-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41951-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41951-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41951-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="41951-108">Type: **LONG**</span></span>

<span data-ttu-id="41951-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="41951-109">Currently unused.</span></span> <span data-ttu-id="41951-110">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="41951-110">Should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41951-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41951-111">Return value</span></span>

<span data-ttu-id="41951-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="41951-112">Type: **HRESULT**</span></span>

<span data-ttu-id="41951-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="41951-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41951-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41951-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="41951-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="41951-115">Remarks</span></span>

<span data-ttu-id="41951-116">O sistema de tempo de execução da Windows Image Acquisition (WIA) 2,0 representa cada dispositivo de hardware WIA 2,0 conectado ao computador do usuário como uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="41951-116">The Windows Image Acquisition (WIA) 2.0 run-time system represents each WIA 2.0 hardware device connected to the user's computer as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="41951-117">Um determinado dispositivo WIA 2,0 pode ou não permitir que aplicativos excluam objetos **IWiaItem2** de sua árvore.</span><span class="sxs-lookup"><span data-stu-id="41951-117">A given WIA 2.0 device may or may not allow applications to delete **IWiaItem2** objects from its tree.</span></span> <span data-ttu-id="41951-118">Itens que têm filhos não podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="41951-118">Items that have children cannot be deleted.</span></span> <span data-ttu-id="41951-119">A interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) deve ser usada para consultar o dispositivo para a funcionalidade de exclusão de itens.</span><span class="sxs-lookup"><span data-stu-id="41951-119">The [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface must be used to query the device for item deletion capability.</span></span>

<span data-ttu-id="41951-120">Se o dispositivo der suporte à exclusão de itens em sua árvore [**IWiaItem2**](-wia-iwiaitem2.md) , chame o método **IWiaItem2::D eleteitem** para remover o objeto **IWiaItem2** .</span><span class="sxs-lookup"><span data-stu-id="41951-120">If the device supports item deletion in its [**IWiaItem2**](-wia-iwiaitem2.md) tree, call the **IWiaItem2::DeleteItem** method to remove the **IWiaItem2** object.</span></span> <span data-ttu-id="41951-121">Observe que esse método só exclui um objeto depois que todas as referências ao objeto forem liberadas.</span><span class="sxs-lookup"><span data-stu-id="41951-121">Note that this method only deletes an object after all references to the object have been released.</span></span> <span data-ttu-id="41951-122">Se a exclusão de um item tiver falhado, E \_ DELETEITEM será retornado.</span><span class="sxs-lookup"><span data-stu-id="41951-122">If the deletion of an item has failed, E\_DELETEITEM is returned.</span></span> <span data-ttu-id="41951-123">O valor numérico para esse erro ainda não foi definido.</span><span class="sxs-lookup"><span data-stu-id="41951-123">The numeric value for this error is not yet defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="41951-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41951-124">Requirements</span></span>



| <span data-ttu-id="41951-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="41951-125">Requirement</span></span> | <span data-ttu-id="41951-126">Valor</span><span class="sxs-lookup"><span data-stu-id="41951-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41951-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41951-127">Minimum supported client</span></span><br/> | <span data-ttu-id="41951-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41951-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="41951-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41951-129">Minimum supported server</span></span><br/> | <span data-ttu-id="41951-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41951-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="41951-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41951-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="41951-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="41951-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="41951-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="41951-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41951-134"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41951-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 




