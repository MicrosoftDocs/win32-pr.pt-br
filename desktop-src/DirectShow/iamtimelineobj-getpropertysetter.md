---
description: O método GetPropertySetter recupera o setter da Propriedade do objeto. Quando o objeto é renderizado, as informações de propriedade contidas no setter da propriedade são aplicadas ao objeto.
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: 'Método IAMTimelineObj:: GetPropertySetter (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4410a0b63a0228d9e8e403ef1f0403d1968ad639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812983"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a><span data-ttu-id="e3bea-104">Método IAMTimelineObj:: GetPropertySetter</span><span class="sxs-lookup"><span data-stu-id="e3bea-104">IAMTimelineObj::GetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="e3bea-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="e3bea-105">\[Deprecated.</span></span> <span data-ttu-id="e3bea-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e3bea-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e3bea-107">O `GetPropertySetter` método recupera o setter da Propriedade do objeto.</span><span class="sxs-lookup"><span data-stu-id="e3bea-107">The `GetPropertySetter` method retrieves the object's property setter.</span></span> <span data-ttu-id="e3bea-108">Quando o objeto é renderizado, as informações de propriedade contidas no setter da propriedade são aplicadas ao objeto.</span><span class="sxs-lookup"><span data-stu-id="e3bea-108">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3bea-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3bea-109">Syntax</span></span>


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e3bea-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3bea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3bea-111">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e3bea-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e3bea-112">Recebe um ponteiro para a interface [**IPropertySetter**](ipropertysetter.md) do setter da propriedade.</span><span class="sxs-lookup"><span data-stu-id="e3bea-112">Receives a pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="e3bea-113">Se o objeto não tiver um setter de propriedade, o valor será definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e3bea-113">If the object does not have a property setter, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3bea-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3bea-114">Return value</span></span>

<span data-ttu-id="e3bea-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e3bea-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3bea-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3bea-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3bea-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3bea-117">Remarks</span></span>

<span data-ttu-id="e3bea-118">Se o valor retornado em *PVal* não for **NULL**, a interface **IPropertySetter** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="e3bea-118">If the value returned in *pVal* is not **NULL**, the **IPropertySetter** interface has an outstanding reference count.</span></span> <span data-ttu-id="e3bea-119">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="e3bea-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="e3bea-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="e3bea-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e3bea-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e3bea-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e3bea-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e3bea-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e3bea-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3bea-123">Requirements</span></span>



| <span data-ttu-id="e3bea-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3bea-124">Requirement</span></span> | <span data-ttu-id="e3bea-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e3bea-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3bea-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3bea-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e3bea-127"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3bea-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e3bea-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3bea-128">Library</span></span><br/> | <dl> <span data-ttu-id="e3bea-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3bea-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3bea-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3bea-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3bea-131">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="e3bea-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="e3bea-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="e3bea-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




