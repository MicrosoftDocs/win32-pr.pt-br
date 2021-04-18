---
description: O método SetRenderRange define o intervalo de tempo na linha do tempo a ser renderizado. Os objetos que ficam fora do intervalo especificado não são renderizados e os recursos não são alocados para eles.
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: 'Método IRenderEngine:: SetRenderRange (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e715c2c0077a890948cfd5f5026afe98633325ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758466"
---
# <a name="irenderenginesetrenderrange-method"></a><span data-ttu-id="264b4-104">Método IRenderEngine:: SetRenderRange</span><span class="sxs-lookup"><span data-stu-id="264b4-104">IRenderEngine::SetRenderRange method</span></span>

> [!Note]  
> <span data-ttu-id="264b4-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="264b4-105">\[Deprecated.</span></span> <span data-ttu-id="264b4-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="264b4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="264b4-107">O `SetRenderRange` método define o intervalo de tempo na linha do tempo a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="264b4-107">The `SetRenderRange` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="264b4-108">Os objetos que ficam fora do intervalo especificado não são renderizados e os recursos não são alocados para eles.</span><span class="sxs-lookup"><span data-stu-id="264b4-108">Objects that lie outside the specified range are not rendered, and resources are not allocated for them.</span></span>

## <a name="syntax"></a><span data-ttu-id="264b4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="264b4-109">Syntax</span></span>


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="264b4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="264b4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="264b4-111">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="264b4-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="264b4-112">Hora de início, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="264b4-112">Start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="264b4-113">*Parar*</span><span class="sxs-lookup"><span data-stu-id="264b4-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="264b4-114">Hora de parada, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="264b4-114">Stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="264b4-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="264b4-115">Return value</span></span>

<span data-ttu-id="264b4-116">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="264b4-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="264b4-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="264b4-117">Return code</span></span>                                                                                            | <span data-ttu-id="264b4-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="264b4-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="264b4-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="264b4-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="264b4-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="264b4-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="264b4-121"><dt>**E \_ deve \_ iniciar o \_ renderizador**</dt></span><span class="sxs-lookup"><span data-stu-id="264b4-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="264b4-122">Falha ao inicializar o mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="264b4-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="264b4-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="264b4-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="264b4-124">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="264b4-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="264b4-125">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="264b4-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="264b4-126">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="264b4-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="264b4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="264b4-127">Requirements</span></span>



| <span data-ttu-id="264b4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="264b4-128">Requirement</span></span> | <span data-ttu-id="264b4-129">Valor</span><span class="sxs-lookup"><span data-stu-id="264b4-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="264b4-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="264b4-130">Header</span></span><br/>  | <dl> <span data-ttu-id="264b4-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="264b4-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="264b4-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="264b4-132">Library</span></span><br/> | <dl> <span data-ttu-id="264b4-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="264b4-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="264b4-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="264b4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="264b4-135">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="264b4-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="264b4-136">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="264b4-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




