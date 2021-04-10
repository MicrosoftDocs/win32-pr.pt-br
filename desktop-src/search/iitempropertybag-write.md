---
description: Faz com que uma ou mais propriedades sejam salvas no recipiente de propriedades. A interface IItemPropertyBag tem suporte apenas no Windows XP e no Windows Server 2003 e não deve mais ser usada.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: 'Método IItemPropertyBag:: Write'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7df66487bba0c2bbef40cf3642754dff56f65835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090050"
---
# <a name="iitempropertybagwrite-method"></a><span data-ttu-id="fcc58-104">Método IItemPropertyBag:: Write</span><span class="sxs-lookup"><span data-stu-id="fcc58-104">IItemPropertyBag::Write method</span></span>

<span data-ttu-id="fcc58-105">Faz com que uma ou mais propriedades sejam salvas no recipiente de propriedades.</span><span class="sxs-lookup"><span data-stu-id="fcc58-105">Causes one or more properties to be saved into the property bag.</span></span> <span data-ttu-id="fcc58-106">A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="fcc58-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc58-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcc58-107">Syntax</span></span>


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="fcc58-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcc58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcc58-109">*cProperties* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcc58-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc58-110">O número de propriedades a serem salvas.</span><span class="sxs-lookup"><span data-stu-id="fcc58-110">The number of properties to save.</span></span> <span data-ttu-id="fcc58-111">Esse argumento especifica o número de elementos nas matrizes em *pPropBag* e *pvarValue*.</span><span class="sxs-lookup"><span data-stu-id="fcc58-111">This argument specifies the number of elements in the arrays at *pPropBag* and *pvarValue*.</span></span>

</dd> <dt>

<span data-ttu-id="fcc58-112">*pPropBag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcc58-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc58-113">Ponteiro para uma matriz de estruturas de [**MyProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) que especifica as propriedades a serem salvas.</span><span class="sxs-lookup"><span data-stu-id="fcc58-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="fcc58-114">*pvarValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fcc58-114">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcc58-115">Ponteiro para uma **variante** cujo tipo depende do tipo de dados das informações de propriedade que ela contém.</span><span class="sxs-lookup"><span data-stu-id="fcc58-115">Pointer to a **VARIANT** whose type depends on the data type of the property information that it contains.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcc58-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fcc58-116">Return value</span></span>

<span data-ttu-id="fcc58-117">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fcc58-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="fcc58-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fcc58-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcc58-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcc58-119">Remarks</span></span>

<span data-ttu-id="fcc58-120">A interface [**IItemPropertyBag**](iitempropertybag.md) tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="fcc58-120">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="fcc58-121">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**IItemPropertyBag**](iitempropertybag.md) e as seguintes APIs: as interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISEARCHITEM**](-search-isearchitem.md) , as estruturas [**LINKINFO**](-search-linkinfo.md) e [**MyProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="fcc58-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc58-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcc58-122">Requirements</span></span>



| <span data-ttu-id="fcc58-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcc58-123">Requirement</span></span> | <span data-ttu-id="fcc58-124">Valor</span><span class="sxs-lookup"><span data-stu-id="fcc58-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fcc58-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcc58-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fcc58-126">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="fcc58-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fcc58-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcc58-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fcc58-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fcc58-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fcc58-129">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="fcc58-129">Redistributable</span></span><br/>          | <span data-ttu-id="fcc58-130">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="fcc58-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fcc58-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcc58-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc58-132">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="fcc58-132">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




