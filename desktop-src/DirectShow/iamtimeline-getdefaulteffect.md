---
description: O método GetDefaultEffect recupera o efeito padrão. Se o mecanismo de renderização não puder renderizar um efeito, ele substituirá o efeito padrão.
ms.assetid: 27eec6e8-702f-4e56-8d81-aa0633b8ec68
title: 'Método IAMTimeline:: GetDefaultEffect (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a0b1cf356a9c067ccae246814d2e1f381d7f78e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748999"
---
# <a name="iamtimelinegetdefaulteffect-method"></a><span data-ttu-id="2d004-104">Método IAMTimeline:: GetDefaultEffect</span><span class="sxs-lookup"><span data-stu-id="2d004-104">IAMTimeline::GetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="2d004-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="2d004-105">\[Deprecated.</span></span> <span data-ttu-id="2d004-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2d004-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2d004-107">O `GetDefaultEffect` método recupera o efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="2d004-107">The `GetDefaultEffect` method retrieves the default effect.</span></span> <span data-ttu-id="2d004-108">Se o mecanismo de renderização não puder renderizar um efeito, ele substituirá o efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="2d004-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d004-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d004-109">Syntax</span></span>


```C++
HRESULT GetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="2d004-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d004-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d004-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="2d004-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="2d004-112">Recebe o GUID (identificador global exclusivo) do efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="2d004-112">Receives the globally unique identifier (GUID) of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d004-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d004-113">Return value</span></span>

<span data-ttu-id="2d004-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2d004-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2d004-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2d004-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d004-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d004-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2d004-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="2d004-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2d004-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2d004-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2d004-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2d004-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2d004-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d004-120">Requirements</span></span>



| <span data-ttu-id="2d004-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d004-121">Requirement</span></span> | <span data-ttu-id="2d004-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2d004-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d004-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d004-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2d004-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d004-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2d004-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d004-125">Library</span></span><br/> | <dl> <span data-ttu-id="2d004-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d004-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d004-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d004-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d004-128">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="2d004-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="2d004-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="2d004-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




