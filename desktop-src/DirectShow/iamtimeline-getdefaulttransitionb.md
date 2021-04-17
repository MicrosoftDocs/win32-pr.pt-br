---
description: 'O método GetDefaultTransitionB recupera a transição padrão. Esse método é equivalente a IAMTimeline:: GetDefaultTransition, mas recebe um valor BSTR, em vez de um GUID.'
ms.assetid: ed743766-e970-4bd9-a9a0-8b5d9fec2d80
title: 'Método IAMTimeline:: GetDefaultTransitionB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f150ca0fafff6b250776a38b7ec68beb470e9d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779538"
---
# <a name="iamtimelinegetdefaulttransitionb-method"></a><span data-ttu-id="89d85-104">Método IAMTimeline:: GetDefaultTransitionB</span><span class="sxs-lookup"><span data-stu-id="89d85-104">IAMTimeline::GetDefaultTransitionB method</span></span>

> [!Note]  
> <span data-ttu-id="89d85-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="89d85-105">\[Deprecated.</span></span> <span data-ttu-id="89d85-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="89d85-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="89d85-107">O `GetDefaultTransitionB` método recupera a transição padrão.</span><span class="sxs-lookup"><span data-stu-id="89d85-107">The `GetDefaultTransitionB` method retrieves the default transition.</span></span> <span data-ttu-id="89d85-108">Esse método é equivalente a [**IAMTimeline:: GetDefaultTransition**](iamtimeline-getdefaulttransition.md), mas recebe um valor BSTR, em vez de um GUID.</span><span class="sxs-lookup"><span data-stu-id="89d85-108">This method is equivalent to [**IAMTimeline::GetDefaultTransition**](iamtimeline-getdefaulttransition.md), but receives a BSTR value, rather than a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d85-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89d85-109">Syntax</span></span>


```C++
HRESULT GetDefaultTransitionB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="89d85-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89d85-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89d85-111">*pGuid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="89d85-111">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="89d85-112">Recebe um valor **BSTR** que representa o GUID da transição padrão.</span><span class="sxs-lookup"><span data-stu-id="89d85-112">Receives a **BSTR** value representing the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89d85-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89d85-113">Return value</span></span>

<span data-ttu-id="89d85-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="89d85-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="89d85-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89d85-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="89d85-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="89d85-116">Remarks</span></span>

<span data-ttu-id="89d85-117">O método aloca memória para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="89d85-117">The method allocates memory for the string.</span></span> <span data-ttu-id="89d85-118">O aplicativo deve chamar **SysFreeString** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="89d85-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="89d85-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="89d85-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="89d85-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="89d85-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="89d85-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="89d85-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="89d85-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89d85-122">Requirements</span></span>



| <span data-ttu-id="89d85-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="89d85-123">Requirement</span></span> | <span data-ttu-id="89d85-124">Valor</span><span class="sxs-lookup"><span data-stu-id="89d85-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89d85-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89d85-125">Header</span></span><br/>  | <dl> <span data-ttu-id="89d85-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="89d85-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="89d85-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89d85-127">Library</span></span><br/> | <dl> <span data-ttu-id="89d85-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89d85-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89d85-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="89d85-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d85-130">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="89d85-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="89d85-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="89d85-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




