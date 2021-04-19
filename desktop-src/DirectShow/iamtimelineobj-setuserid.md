---
description: O método setUserID define um identificador definido pelo aplicativo para o objeto.
ms.assetid: 102fe29e-dc2c-4377-bce3-ba3c61dcb355
title: 'Método IAMTimelineObj:: setUserID (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 31a0c59c6c93535be1200b2cd7678d4c355b5bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782843"
---
# <a name="iamtimelineobjsetuserid-method"></a><span data-ttu-id="2221f-103">Método IAMTimelineObj:: setUserID</span><span class="sxs-lookup"><span data-stu-id="2221f-103">IAMTimelineObj::SetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="2221f-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="2221f-104">\[Deprecated.</span></span> <span data-ttu-id="2221f-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2221f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2221f-106">O `SetUserID` método define um identificador definido pelo aplicativo para o objeto.</span><span class="sxs-lookup"><span data-stu-id="2221f-106">The `SetUserID` method sets an application-defined identifier for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2221f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2221f-107">Syntax</span></span>


```C++
HRESULT SetUserID(
   long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="2221f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2221f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2221f-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="2221f-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="2221f-110">Valor que especifica o identificador.</span><span class="sxs-lookup"><span data-stu-id="2221f-110">Value that specifies the identifier.</span></span> <span data-ttu-id="2221f-111">Esse identificador é usado somente pelo aplicativo e pode ser qualquer valor.</span><span class="sxs-lookup"><span data-stu-id="2221f-111">This identifier is used only by the application and can be any value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2221f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2221f-112">Return value</span></span>

<span data-ttu-id="2221f-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2221f-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2221f-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2221f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2221f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2221f-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2221f-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="2221f-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2221f-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2221f-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2221f-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2221f-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2221f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2221f-119">Requirements</span></span>



| <span data-ttu-id="2221f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2221f-120">Requirement</span></span> | <span data-ttu-id="2221f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2221f-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2221f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2221f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2221f-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2221f-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2221f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2221f-124">Library</span></span><br/> | <dl> <span data-ttu-id="2221f-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2221f-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2221f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2221f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2221f-127">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="2221f-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="2221f-128">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="2221f-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




