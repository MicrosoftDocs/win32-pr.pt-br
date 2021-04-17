---
description: Obtém as informações necessárias para ler ou salvar as propriedades no recipiente de propriedades. A interface IItemPropertyBag tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: 'Método IItemPropertyBag:: GetPropertyInfo'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762134"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a><span data-ttu-id="0f185-104">Método IItemPropertyBag:: GetPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="0f185-104">IItemPropertyBag::GetPropertyInfo method</span></span>

<span data-ttu-id="0f185-105">Obtém as informações necessárias para ler ou salvar as propriedades no recipiente de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0f185-105">Gets the information required to read or save the properties in the property bag.</span></span> <span data-ttu-id="0f185-106">A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="0f185-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f185-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f185-107">Syntax</span></span>


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a><span data-ttu-id="0f185-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f185-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f185-109">*iProperty* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f185-109">*iProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f185-110">O índice de base zero da primeira propriedade para a qual as informações são solicitadas.</span><span class="sxs-lookup"><span data-stu-id="0f185-110">The zero-based index of the first property for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="0f185-111">*cProperties* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f185-111">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f185-112">O número de propriedades para as quais obter informações.</span><span class="sxs-lookup"><span data-stu-id="0f185-112">The number of properties to get information for.</span></span> <span data-ttu-id="0f185-113">Esse argumento especifica o número de elementos de matriz em *pPropBag*.</span><span class="sxs-lookup"><span data-stu-id="0f185-113">This argument specifies the number of array elements in *pPropBag*.</span></span>

</dd> <dt>

<span data-ttu-id="0f185-114">*pPropBag* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f185-114">*pPropBag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f185-115">Ponteiro para uma matriz de estruturas do [**doprop**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que recebe as informações para as propriedades.</span><span class="sxs-lookup"><span data-stu-id="0f185-115">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that receives the information for the properties.</span></span>

</dd> <dt>

<span data-ttu-id="0f185-116">*pcProperties* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f185-116">*pcProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f185-117">Recebe um ponteiro para uma variável **ULONG** que recebe o número de propriedades para as quais as informações foram recuperadas.</span><span class="sxs-lookup"><span data-stu-id="0f185-117">Receives a pointer to a **ULONG** variable that receives the number of properties for which information was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f185-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f185-118">Return value</span></span>

<span data-ttu-id="0f185-119">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0f185-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="0f185-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f185-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f185-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f185-121">Remarks</span></span>

<span data-ttu-id="0f185-122">A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="0f185-122">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="0f185-123">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPropertyBag**](iitempropertybag.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISEARCHITEM**](-search-isearchitem.md) , as estruturas [**LINKINFO**](-search-linkinfo.md) e [**MyProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="0f185-123">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f185-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f185-124">Requirements</span></span>



| <span data-ttu-id="0f185-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f185-125">Requirement</span></span> | <span data-ttu-id="0f185-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0f185-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0f185-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f185-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0f185-128">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="0f185-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0f185-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f185-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0f185-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f185-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0f185-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="0f185-131">Redistributable</span></span><br/>          | <span data-ttu-id="0f185-132">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="0f185-132">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="0f185-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f185-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f185-134">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="0f185-134">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




