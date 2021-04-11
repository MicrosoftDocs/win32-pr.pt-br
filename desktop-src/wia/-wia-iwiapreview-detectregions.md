---
description: 'Invoca o filtro de segmentação de driver e passa a imagem não filtrada armazenada em cache pelo método IWiaPreview:: GetNewPreview para o filtro.'
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: 'IWiaPreview: método etectRegions de:D (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 40665d2aae6e1e2dffa4356540afb05d45050492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164533"
---
# <a name="iwiapreviewdetectregions-method"></a><span data-ttu-id="63837-103">IWiaPreview: método etectRegions de:D</span><span class="sxs-lookup"><span data-stu-id="63837-103">IWiaPreview::DetectRegions method</span></span>

<span data-ttu-id="63837-104">Invoca o filtro de segmentação de driver e passa a imagem não filtrada armazenada em cache pelo método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) para o filtro.</span><span class="sxs-lookup"><span data-stu-id="63837-104">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="63837-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63837-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="63837-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63837-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63837-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63837-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63837-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="63837-108">Type: **LONG**</span></span>

<span data-ttu-id="63837-109">Não usado.</span><span class="sxs-lookup"><span data-stu-id="63837-109">Not used.</span></span> <span data-ttu-id="63837-110">Defina como zero (0).</span><span class="sxs-lookup"><span data-stu-id="63837-110">Set to zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63837-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63837-111">Return value</span></span>

<span data-ttu-id="63837-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="63837-112">Type: **HRESULT**</span></span>

<span data-ttu-id="63837-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="63837-113">This method can return one of these values.</span></span>



| <span data-ttu-id="63837-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="63837-114">Return code</span></span>                                                                               | <span data-ttu-id="63837-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="63837-115">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="63837-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63837-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="63837-117">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="63837-117">The operation is successful.</span></span><br/>              |
| <dl> <span data-ttu-id="63837-118"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="63837-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="63837-119">O driver não dá suporte à segmentação.</span><span class="sxs-lookup"><span data-stu-id="63837-119">The driver does not support segmentation.</span></span><br/> |
| <dl> <span data-ttu-id="63837-120"><dt>**,**</dt></span><span class="sxs-lookup"><span data-stu-id="63837-120"><dt>**otherwise**</dt></span></span> </dl>  | <span data-ttu-id="63837-121">Um código de erro COM padrão.</span><span class="sxs-lookup"><span data-stu-id="63837-121">A standard COM error code.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="63837-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="63837-122">Remarks</span></span>

<span data-ttu-id="63837-123">Um aplicativo deve chamar [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) antes de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="63837-123">An application must call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) before it calls this function.</span></span>

<span data-ttu-id="63837-124">Quando o componente de versão prévia do WIA (Windows Image Acquisition) 2,0 chama **IWiaPreview::D etectregions**, ele invoca o filtro de segmentação de driver e passa a interface [**IWiaItem2**](-wia-iwiaitem2.md) que foi passada anteriormente para [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="63837-124">When the Windows Image Acquisition (WIA) 2.0 Preview Component calls **IWiaPreview::DetectRegions**, it invokes the driver segmentation filter and passes the [**IWiaItem2**](-wia-iwiaitem2.md) interface that was previously passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="63837-125">Ele também passa a imagem armazenada internamente em cache para o filtro.</span><span class="sxs-lookup"><span data-stu-id="63837-125">It also passes the internally cached image to the filter.</span></span> <span data-ttu-id="63837-126">O filtro de segmentação usa a imagem armazenada em cache para criar as extensões filhas.</span><span class="sxs-lookup"><span data-stu-id="63837-126">The segmentation filter uses the cached image to create the child extents.</span></span>

<span data-ttu-id="63837-127">Se um aplicativo alterar as propriedades da interface [**IWiaItem2**](-wia-iwiaitem2.md) depois de chamar [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md), as propriedades originais deverão ser restauradas antes que o aplicativo chame **IWiaPreview::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="63837-127">If an application changes any properties of the [**IWiaItem2**](-wia-iwiaitem2.md) interface after it calls [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md), then the original properties must be restored before the application calls **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="63837-128">Use [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) e [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) para restaurar as propriedades originais.</span><span class="sxs-lookup"><span data-stu-id="63837-128">Use [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) to restore the original properties.</span></span>

<span data-ttu-id="63837-129">**IWiaPreview::D etectregions** é usado para determinar as "subregiãos" da imagem armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="63837-129">**IWiaPreview::DetectRegions** is used to determine the "sub-regions" of the cached image.</span></span> <span data-ttu-id="63837-130">Para cada sub-região detectada, um novo item filho WIA 2,0 é criado na interface [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="63837-130">For each sub-region detected, a new child WIA 2.0 item is created under the [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span> <span data-ttu-id="63837-131">Para cada item filho, o filtro de segmentação deve definir os valores para as seguintes propriedades WIA 2,0: WIA \_ IPS \_ XPos, WIA \_ IPS \_ YPos, WIA \_ IPS XEXTENT e \_ WIA \_ IPS \_ YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="63837-131">For each child item, the segmentation filter must set the values for the following WIA 2.0 properties: WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT.</span></span> <span data-ttu-id="63837-132">Um filtro mais avançado define outras propriedades de WIA 2,0, como \_ os IPs WIA distorção \_ \_ X e WIA IPS de \_ distorção \_ \_ Y, se o driver oferecer suporte à remoção de distorção.</span><span class="sxs-lookup"><span data-stu-id="63837-132">A more advanced filter sets other WIA 2.0 properties, such as WIA\_IPS\_DESKEW\_X and WIA\_IPS\_DESKEW\_Y, if the driver supports de-skewing.</span></span> <span data-ttu-id="63837-133">Os IPs \_ WIA \_ XPos, WIA \_ IPS \_ YPos, WIA \_ IPS \_ XEXTENT e \_ \_ as propriedades YEXTENT IPS WIA representam o retângulo delimitador da área a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="63837-133">The WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT properties represent the bounding rectangle of the area to scan.</span></span>

<span data-ttu-id="63837-134">O driver pode não dar suporte à segmentação.</span><span class="sxs-lookup"><span data-stu-id="63837-134">The driver might not support segmentation.</span></span> <span data-ttu-id="63837-135">Antes de chamar **IWiaPreview::D etectregions**, um aplicativo geralmente verifica se o driver dá suporte \_ à \_ propriedade de segmentação de IPS WIA.</span><span class="sxs-lookup"><span data-stu-id="63837-135">Before calling **IWiaPreview::DetectRegions**, an application typically checks whether the driver supports the WIA\_IPS\_SEGMENTATION property.</span></span> <span data-ttu-id="63837-136">Se a propriedade não for implementada, a segmentação não terá suporte e **IWiaPreview::D etectregions** falhará E retornará e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="63837-136">If the property is not implemented, segmentation is not supported, and **IWiaPreview::DetectRegions** fails and returns E\_NOTIMPL.</span></span>

<span data-ttu-id="63837-137">O aplicativo deve limpar os itens filho que são criados chamando **IWiaPreview::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="63837-137">The application must clean up the child items that are created by calling **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="63837-138">Por exemplo, se um aplicativo fizer uma chamada adicional para **IWiaPreview::D etectregions** no mesmo item, ele deverá limpar os itens filho anteriores.</span><span class="sxs-lookup"><span data-stu-id="63837-138">For example, if an application makes an additional call to **IWiaPreview::DetectRegions** on the same item, it must clean up the previous child items.</span></span>

## <a name="requirements"></a><span data-ttu-id="63837-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63837-139">Requirements</span></span>



| <span data-ttu-id="63837-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="63837-140">Requirement</span></span> | <span data-ttu-id="63837-141">Valor</span><span class="sxs-lookup"><span data-stu-id="63837-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63837-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63837-142">Minimum supported client</span></span><br/> | <span data-ttu-id="63837-143">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63837-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="63837-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63837-144">Minimum supported server</span></span><br/> | <span data-ttu-id="63837-145">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63837-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="63837-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63837-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="63837-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="63837-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="63837-148">INSERI</span><span class="sxs-lookup"><span data-stu-id="63837-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63837-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63837-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 




