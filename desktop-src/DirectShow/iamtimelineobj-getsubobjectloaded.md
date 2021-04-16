---
description: O método GetSubObjectLoaded determina se o ponteiro do subobjeto foi definido.
ms.assetid: 05b58435-eeca-4b52-9a53-ad7f81b5b35d
title: 'Método IAMTimelineObj:: GetSubObjectLoaded (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectLoaded
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 073810b6c02997d78e21a66976954d88e47ae82b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757887"
---
# <a name="iamtimelineobjgetsubobjectloaded-method"></a><span data-ttu-id="41da3-103">Método IAMTimelineObj:: GetSubObjectLoaded</span><span class="sxs-lookup"><span data-stu-id="41da3-103">IAMTimelineObj::GetSubObjectLoaded method</span></span>

> [!Note]  
> <span data-ttu-id="41da3-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="41da3-104">\[Deprecated.</span></span> <span data-ttu-id="41da3-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="41da3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="41da3-106">O `GetSubObjectLoaded` método determina se o ponteiro do subobjeto foi definido.</span><span class="sxs-lookup"><span data-stu-id="41da3-106">The `GetSubObjectLoaded` method determines whether the subobject pointer has been set.</span></span>

## <a name="syntax"></a><span data-ttu-id="41da3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41da3-107">Syntax</span></span>


```C++
HRESULT GetSubObjectLoaded(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="41da3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41da3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41da3-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="41da3-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="41da3-110">Recebe um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="41da3-110">Receives a Boolean value.</span></span> <span data-ttu-id="41da3-111">Se o valor for **true**, o ponteiro do subobjeto foi definido.</span><span class="sxs-lookup"><span data-stu-id="41da3-111">If the value is **TRUE**, the subobject pointer has been set.</span></span> <span data-ttu-id="41da3-112">Se **for false**, o ponteiro não foi definido.</span><span class="sxs-lookup"><span data-stu-id="41da3-112">If **FALSE**, the pointer has not been set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41da3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41da3-113">Return value</span></span>

<span data-ttu-id="41da3-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="41da3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41da3-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41da3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="41da3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="41da3-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="41da3-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="41da3-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="41da3-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="41da3-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="41da3-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="41da3-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="41da3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41da3-120">Requirements</span></span>



| <span data-ttu-id="41da3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="41da3-121">Requirement</span></span> | <span data-ttu-id="41da3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="41da3-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41da3-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41da3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="41da3-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="41da3-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="41da3-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41da3-125">Library</span></span><br/> | <dl> <span data-ttu-id="41da3-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41da3-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41da3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="41da3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41da3-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="41da3-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="41da3-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="41da3-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




