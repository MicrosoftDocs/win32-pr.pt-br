---
description: O método GetGenID recupera o identificador gerado do objeto. O identificador é um número reservado; os aplicativos não devem usá-lo.
ms.assetid: b71b9b52-589b-4f80-915f-4805b1b8e295
title: 'Método IAMTimelineObj:: GetGenID (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGenID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3497777d25c9a81d4334f1979ce33f351111ed4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778474"
---
# <a name="iamtimelineobjgetgenid-method"></a><span data-ttu-id="46cf0-104">Método IAMTimelineObj:: GetGenID</span><span class="sxs-lookup"><span data-stu-id="46cf0-104">IAMTimelineObj::GetGenID method</span></span>

> [!Note]  
> <span data-ttu-id="46cf0-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="46cf0-105">\[Deprecated.</span></span> <span data-ttu-id="46cf0-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="46cf0-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="46cf0-107">O `GetGenID` método recupera o identificador gerado do objeto.</span><span class="sxs-lookup"><span data-stu-id="46cf0-107">The `GetGenID` method retrieves the object's generated identifier.</span></span> <span data-ttu-id="46cf0-108">O identificador é um número reservado; os aplicativos não devem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="46cf0-108">The identifier is a reserved number; applications should not use it.</span></span>

## <a name="syntax"></a><span data-ttu-id="46cf0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46cf0-109">Syntax</span></span>


```C++
HRESULT GetGenID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="46cf0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46cf0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46cf0-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="46cf0-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="46cf0-112">Recebe o identificador gerado.</span><span class="sxs-lookup"><span data-stu-id="46cf0-112">Receives the generated identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46cf0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="46cf0-113">Return value</span></span>

<span data-ttu-id="46cf0-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="46cf0-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46cf0-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46cf0-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46cf0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="46cf0-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="46cf0-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="46cf0-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="46cf0-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="46cf0-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="46cf0-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="46cf0-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46cf0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46cf0-120">Requirements</span></span>



| <span data-ttu-id="46cf0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="46cf0-121">Requirement</span></span> | <span data-ttu-id="46cf0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="46cf0-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46cf0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46cf0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="46cf0-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="46cf0-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="46cf0-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46cf0-125">Library</span></span><br/> | <dl> <span data-ttu-id="46cf0-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46cf0-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46cf0-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="46cf0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46cf0-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="46cf0-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="46cf0-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="46cf0-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




