---
description: Faz com que uma ou mais propriedades sejam lidas do recipiente de propriedades. A interface IItemPropertyBag tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: 'Método IItemPropertyBag:: Read'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7af13dc42239a2823d7e7ca9b8def4748519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296237"
---
# <a name="iitempropertybagread-method"></a><span data-ttu-id="07d0e-104">Método IItemPropertyBag:: Read</span><span class="sxs-lookup"><span data-stu-id="07d0e-104">IItemPropertyBag::Read method</span></span>

<span data-ttu-id="07d0e-105">Faz com que uma ou mais propriedades sejam lidas do recipiente de propriedades.</span><span class="sxs-lookup"><span data-stu-id="07d0e-105">Causes one or more properties to be read from the property bag.</span></span> <span data-ttu-id="07d0e-106">A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="07d0e-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d0e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07d0e-107">Syntax</span></span>


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a><span data-ttu-id="07d0e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07d0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d0e-109">*cProperties* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07d0e-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d0e-110">O número de propriedades a serem lidas.</span><span class="sxs-lookup"><span data-stu-id="07d0e-110">The number of properties to read.</span></span> <span data-ttu-id="07d0e-111">Esse argumento especifica o número de elementos nas matrizes em *pPropBag*, *pvarValue* e *phrError*.</span><span class="sxs-lookup"><span data-stu-id="07d0e-111">This argument specifies the number of elements in the arrays at *pPropBag*, *pvarValue*, and *phrError*.</span></span>

</dd> <dt>

<span data-ttu-id="07d0e-112">*pPropBag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07d0e-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d0e-113">Ponteiro para uma matriz de estruturas de [**MyProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que especifica as propriedades que são solicitadas.</span><span class="sxs-lookup"><span data-stu-id="07d0e-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties that are requested.</span></span>

</dd> <dt>

<span data-ttu-id="07d0e-114">*pvarValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="07d0e-114">*pvarValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07d0e-115">Recebe um ponteiro que retorna uma matriz de estruturas **Variant** que recebe os valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="07d0e-115">Receives a pointer that returns an array of **VARIANT** structures that receives the property values.</span></span>

</dd> <dt>

<span data-ttu-id="07d0e-116">*phrError* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="07d0e-116">*phrError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07d0e-117">Ponteiro para uma matriz de valores **HRESULT** que recebe o resultado de cada propriedade lida.</span><span class="sxs-lookup"><span data-stu-id="07d0e-117">Pointer to an array of **HRESULT** values that receives the result of each property read.</span></span> <span data-ttu-id="07d0e-118">Deve haver pelo menos elementos *cProperties* nesta matriz.</span><span class="sxs-lookup"><span data-stu-id="07d0e-118">There must be at least *cProperties* elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d0e-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07d0e-119">Return value</span></span>

<span data-ttu-id="07d0e-120">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="07d0e-120">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="07d0e-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07d0e-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="07d0e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="07d0e-122">Remarks</span></span>

<span data-ttu-id="07d0e-123">A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="07d0e-123">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="07d0e-124">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPropertyBag**](iitempropertybag.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISEARCHITEM**](-search-isearchitem.md) , as estruturas [**LINKINFO**](-search-linkinfo.md) e [**MyProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="07d0e-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="07d0e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07d0e-125">Requirements</span></span>



| <span data-ttu-id="07d0e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="07d0e-126">Requirement</span></span> | <span data-ttu-id="07d0e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="07d0e-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07d0e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07d0e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="07d0e-129">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="07d0e-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="07d0e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07d0e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="07d0e-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="07d0e-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="07d0e-132">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="07d0e-132">Redistributable</span></span><br/>          | <span data-ttu-id="07d0e-133">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="07d0e-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="07d0e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="07d0e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d0e-135">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="07d0e-135">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




