---
description: O método gettimelinetype recupera o tipo do objeto.
ms.assetid: db46457f-25d0-4421-af73-426d65b720d3
title: 'Método IAMTimelineObj:: gettimelinetype (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76b9c2a847cc0d0150b21062810290aaaab702cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785493"
---
# <a name="iamtimelineobjgettimelinetype-method"></a><span data-ttu-id="ca53e-103">Método IAMTimelineObj:: gettimelinetype</span><span class="sxs-lookup"><span data-stu-id="ca53e-103">IAMTimelineObj::GetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="ca53e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="ca53e-104">\[Deprecated.</span></span> <span data-ttu-id="ca53e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ca53e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ca53e-106">O `GetTimelineType` método recupera o tipo do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca53e-106">The `GetTimelineType` method retrieves the object's type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca53e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca53e-107">Syntax</span></span>


```C++
HRESULT GetTimelineType(
   TIMELINE_MAJOR_TYPE *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ca53e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca53e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca53e-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="ca53e-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="ca53e-110">Recebe um membro do tipo enumerado de [**\_ \_ tipo principal da linha do tempo**](timeline-major-type.md) , indicando o tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="ca53e-110">Receives a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, indicating the type of object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca53e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca53e-111">Return value</span></span>

<span data-ttu-id="ca53e-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ca53e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ca53e-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ca53e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca53e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca53e-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ca53e-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="ca53e-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ca53e-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ca53e-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ca53e-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ca53e-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ca53e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca53e-118">Requirements</span></span>



| <span data-ttu-id="ca53e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca53e-119">Requirement</span></span> | <span data-ttu-id="ca53e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ca53e-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca53e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca53e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ca53e-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca53e-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ca53e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca53e-123">Library</span></span><br/> | <dl> <span data-ttu-id="ca53e-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca53e-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca53e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca53e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca53e-126">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="ca53e-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="ca53e-127">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="ca53e-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




