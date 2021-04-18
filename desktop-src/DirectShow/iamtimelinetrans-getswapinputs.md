---
description: O método GetSwapInputs recupera um valor que indica se as entradas de transição são trocadas.
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: 'Método IAMTimelineTrans:: GetSwapInputs (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a2acdff1007bd26773ce495d024676632eee1767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810938"
---
# <a name="iamtimelinetransgetswapinputs-method"></a><span data-ttu-id="26284-103">Método IAMTimelineTrans:: GetSwapInputs</span><span class="sxs-lookup"><span data-stu-id="26284-103">IAMTimelineTrans::GetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="26284-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="26284-104">\[Deprecated.</span></span> <span data-ttu-id="26284-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="26284-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="26284-106">O `GetSwapInputs` método recupera um valor que indica se as entradas de transição são trocadas.</span><span class="sxs-lookup"><span data-stu-id="26284-106">The `GetSwapInputs` method retrieves a value that indicates whether the transition inputs are swapped.</span></span>

<span data-ttu-id="26284-107">Por padrão, uma transição é proveniente da composição de todas as camadas de prioridade inferior para a camada em que reside a transição.</span><span class="sxs-lookup"><span data-stu-id="26284-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="26284-108">Você pode reverter essa progressão, de modo que a transição vai da camada onde ela reside de volta para a composição de camadas de prioridade inferior.</span><span class="sxs-lookup"><span data-stu-id="26284-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span>

## <a name="syntax"></a><span data-ttu-id="26284-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26284-109">Syntax</span></span>


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="26284-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26284-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26284-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="26284-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="26284-112">Recebe um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="26284-112">Receives a Boolean value.</span></span> <span data-ttu-id="26284-113">Se o valor for **false**, a transição passará da composição de todas as camadas de prioridade inferior para a camada de transição.</span><span class="sxs-lookup"><span data-stu-id="26284-113">If the value is **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="26284-114">Se o valor for **true**, a transição irá para a direção oposta.</span><span class="sxs-lookup"><span data-stu-id="26284-114">If the value is **TRUE**, the transition goes in the opposite direction.</span></span> <span data-ttu-id="26284-115">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="26284-115">The default value is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26284-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26284-116">Return value</span></span>

<span data-ttu-id="26284-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="26284-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26284-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26284-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="26284-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="26284-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="26284-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="26284-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="26284-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="26284-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="26284-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="26284-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26284-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26284-123">Requirements</span></span>



| <span data-ttu-id="26284-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="26284-124">Requirement</span></span> | <span data-ttu-id="26284-125">Valor</span><span class="sxs-lookup"><span data-stu-id="26284-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26284-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26284-126">Header</span></span><br/>  | <dl> <span data-ttu-id="26284-127"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="26284-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="26284-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26284-128">Library</span></span><br/> | <dl> <span data-ttu-id="26284-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26284-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26284-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="26284-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26284-131">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="26284-131">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="26284-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="26284-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




