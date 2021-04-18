---
description: 'O método SetRenderRange2 define o intervalo de tempo na linha do tempo a ser renderizado. Esse método é equivalente a IRenderEngine:: SetRenderRange, mas obtém valores do tipo Double.'
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: 'Método IRenderEngine:: SetRenderRange2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 555533b11c96073763af0d2b52823af44e3797be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786966"
---
# <a name="irenderenginesetrenderrange2-method"></a><span data-ttu-id="53206-104">Método IRenderEngine:: SetRenderRange2</span><span class="sxs-lookup"><span data-stu-id="53206-104">IRenderEngine::SetRenderRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="53206-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="53206-105">\[Deprecated.</span></span> <span data-ttu-id="53206-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53206-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="53206-107">O `SetRenderRange2` método define o intervalo de tempo na linha do tempo a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="53206-107">The `SetRenderRange2` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="53206-108">Esse método é equivalente a [**IRenderEngine:: SetRenderRange**](irenderengine-setrenderrange.md), mas obtém valores do tipo **Double**.</span><span class="sxs-lookup"><span data-stu-id="53206-108">This method is equivalent to [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md), but takes values of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="53206-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53206-109">Syntax</span></span>


```C++
HRESULT SetRenderRange2(
   double Start,
   double Stop
);
```



## <a name="parameters"></a><span data-ttu-id="53206-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53206-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53206-111">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="53206-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="53206-112">Hora de início, em segundos.</span><span class="sxs-lookup"><span data-stu-id="53206-112">Start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="53206-113">*Parar*</span><span class="sxs-lookup"><span data-stu-id="53206-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="53206-114">Hora de parada, em segundos.</span><span class="sxs-lookup"><span data-stu-id="53206-114">Stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53206-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53206-115">Return value</span></span>

<span data-ttu-id="53206-116">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="53206-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="53206-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="53206-117">Return code</span></span>                                                                                            | <span data-ttu-id="53206-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="53206-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="53206-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53206-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="53206-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="53206-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="53206-121"><dt>**E \_ deve \_ iniciar o \_ renderizador**</dt></span><span class="sxs-lookup"><span data-stu-id="53206-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="53206-122">Falha ao inicializar o mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="53206-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="53206-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="53206-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="53206-124">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="53206-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="53206-125">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="53206-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="53206-126">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="53206-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53206-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53206-127">Requirements</span></span>



| <span data-ttu-id="53206-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="53206-128">Requirement</span></span> | <span data-ttu-id="53206-129">Valor</span><span class="sxs-lookup"><span data-stu-id="53206-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53206-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53206-130">Header</span></span><br/>  | <dl> <span data-ttu-id="53206-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="53206-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="53206-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53206-132">Library</span></span><br/> | <dl> <span data-ttu-id="53206-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53206-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53206-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="53206-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53206-135">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="53206-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="53206-136">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="53206-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




