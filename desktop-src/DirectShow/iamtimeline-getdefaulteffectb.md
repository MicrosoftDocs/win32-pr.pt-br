---
description: 'O método GetDefaultEffectB recupera o efeito padrão. Esse método é equivalente a IAMTimeline:: GetDefaultEffect, mas recebe um valor BSTR em vez de um GUID.'
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: 'Método IAMTimeline:: GetDefaultEffectB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 01b82c42c34e3146bbad5560d516aef55225a3d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752876"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a><span data-ttu-id="22aa4-104">Método IAMTimeline:: GetDefaultEffectB</span><span class="sxs-lookup"><span data-stu-id="22aa4-104">IAMTimeline::GetDefaultEffectB method</span></span>

> [!Note]  
> <span data-ttu-id="22aa4-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="22aa4-105">\[Deprecated.</span></span> <span data-ttu-id="22aa4-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="22aa4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="22aa4-107">O `GetDefaultEffectB` método recupera o efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="22aa4-107">The `GetDefaultEffectB` method retrieves the default effect.</span></span> <span data-ttu-id="22aa4-108">Esse método é equivalente a [**IAMTimeline:: GetDefaultEffect**](iamtimeline-getdefaulteffect.md), mas recebe um valor **BSTR** em vez de um GUID.</span><span class="sxs-lookup"><span data-stu-id="22aa4-108">This method is equivalent to [**IAMTimeline::GetDefaultEffect**](iamtimeline-getdefaulteffect.md), but receives a **BSTR** value rather than a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="22aa4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22aa4-109">Syntax</span></span>


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="22aa4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22aa4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22aa4-111">*pGuid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="22aa4-111">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="22aa4-112">Recebe um valor **BSTR** que representa o GUID do efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="22aa4-112">Receives a **BSTR** value representing the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22aa4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22aa4-113">Return value</span></span>

<span data-ttu-id="22aa4-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="22aa4-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22aa4-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22aa4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22aa4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="22aa4-116">Remarks</span></span>

<span data-ttu-id="22aa4-117">O método aloca memória para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="22aa4-117">The method allocates memory for the string.</span></span> <span data-ttu-id="22aa4-118">O aplicativo deve chamar **SysFreeString** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="22aa4-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="22aa4-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="22aa4-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="22aa4-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="22aa4-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="22aa4-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="22aa4-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22aa4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22aa4-122">Requirements</span></span>



| <span data-ttu-id="22aa4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="22aa4-123">Requirement</span></span> | <span data-ttu-id="22aa4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="22aa4-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22aa4-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="22aa4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="22aa4-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="22aa4-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="22aa4-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22aa4-127">Library</span></span><br/> | <dl> <span data-ttu-id="22aa4-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22aa4-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22aa4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="22aa4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22aa4-130">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="22aa4-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="22aa4-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="22aa4-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




