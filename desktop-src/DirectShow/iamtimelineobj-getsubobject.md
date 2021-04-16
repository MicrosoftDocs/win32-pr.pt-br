---
description: O método GetSubObject recupera o subobjeto associado a esse objeto.
ms.assetid: 478597d6-ae13-4fa9-a928-19893f378f1a
title: 'Método IAMTimelineObj:: GetSubObject (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74f14658db5ffbaf100925f26573a08b592f6510
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754248"
---
# <a name="iamtimelineobjgetsubobject-method"></a><span data-ttu-id="311d3-103">Método IAMTimelineObj:: GetSubObject</span><span class="sxs-lookup"><span data-stu-id="311d3-103">IAMTimelineObj::GetSubObject method</span></span>

> [!Note]  
> <span data-ttu-id="311d3-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="311d3-104">\[Deprecated.</span></span> <span data-ttu-id="311d3-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="311d3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="311d3-106">O `GetSubObject` método recupera o subobjeto associado a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="311d3-106">The `GetSubObject` method retrieves the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="311d3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="311d3-107">Syntax</span></span>


```C++
HRESULT GetSubObject(
  [out, retval] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="311d3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="311d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="311d3-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="311d3-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="311d3-110">Recebe um ponteiro para a interface **IUnknown** do subobjeto.</span><span class="sxs-lookup"><span data-stu-id="311d3-110">Receives a pointer to the subobject's **IUnknown** interface.</span></span> <span data-ttu-id="311d3-111">Se o objeto não tiver um subobjeto, o valor será definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="311d3-111">If the object does not have a subobject, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="311d3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="311d3-112">Return value</span></span>

<span data-ttu-id="311d3-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="311d3-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="311d3-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="311d3-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="311d3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="311d3-115">Remarks</span></span>

<span data-ttu-id="311d3-116">Cada objeto Timeline pode conter um ponteiro para um subobjeto associado.</span><span class="sxs-lookup"><span data-stu-id="311d3-116">Every timeline object can hold a pointer to an associated subobject.</span></span>

<span data-ttu-id="311d3-117">Se o valor retornado em *PVal* não for **NULL**, a interface **IUnknown** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="311d3-117">If the value returned in *pVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="311d3-118">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="311d3-118">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="311d3-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="311d3-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="311d3-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="311d3-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="311d3-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="311d3-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="311d3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="311d3-122">Requirements</span></span>



| <span data-ttu-id="311d3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="311d3-123">Requirement</span></span> | <span data-ttu-id="311d3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="311d3-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="311d3-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="311d3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="311d3-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="311d3-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="311d3-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="311d3-127">Library</span></span><br/> | <dl> <span data-ttu-id="311d3-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="311d3-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="311d3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="311d3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="311d3-130">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="311d3-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="311d3-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="311d3-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




