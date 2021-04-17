---
description: O método GetEffect recupera o efeito no nível de prioridade especificado.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'Método IAMTimelineEffectable:: GetEffect (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7a769fca28ea1f8f698b23de7df6b7c15f05234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758521"
---
# <a name="iamtimelineeffectablegeteffect-method"></a><span data-ttu-id="1a062-103">Método IAMTimelineEffectable:: GetEffect</span><span class="sxs-lookup"><span data-stu-id="1a062-103">IAMTimelineEffectable::GetEffect method</span></span>

> [!Note]  
> <span data-ttu-id="1a062-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="1a062-104">\[Deprecated.</span></span> <span data-ttu-id="1a062-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1a062-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1a062-106">O método **GetEffect** recupera o efeito no nível de prioridade especificado.</span><span class="sxs-lookup"><span data-stu-id="1a062-106">The **GetEffect** method retrieves the effect at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a062-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a062-107">Syntax</span></span>


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="1a062-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a062-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a062-109">*ppFX* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1a062-109">*ppFX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a062-110">Recebe a interface [**IAMTimelineObj**](iamtimelineobj.md) do efeito.</span><span class="sxs-lookup"><span data-stu-id="1a062-110">Receives the effect's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1a062-111">*Onde*</span><span class="sxs-lookup"><span data-stu-id="1a062-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="1a062-112">Nível de prioridade do efeito a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="1a062-112">Priority level of the effect to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a062-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a062-113">Return value</span></span>

<span data-ttu-id="1a062-114">Retorna um valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="1a062-114">Returns an HRESULT value.</span></span> <span data-ttu-id="1a062-115">Os possíveis valores incluem os seguintes:</span><span class="sxs-lookup"><span data-stu-id="1a062-115">Possible values include the following:</span></span>



| <span data-ttu-id="1a062-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1a062-116">Return code</span></span>                                                                               | <span data-ttu-id="1a062-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a062-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="1a062-118"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="1a062-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="1a062-119">Sem efeito na prioridade especificada,</span><span class="sxs-lookup"><span data-stu-id="1a062-119">No effect at the specified priority,</span></span><br/> |
| <dl> <span data-ttu-id="1a062-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1a062-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="1a062-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="1a062-121">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="1a062-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="1a062-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="1a062-123">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="1a062-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="1a062-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a062-124">Remarks</span></span>

<span data-ttu-id="1a062-125">Se o método retornar S \_ OK, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="1a062-125">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="1a062-126">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="1a062-126">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="1a062-127">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="1a062-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1a062-128">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a062-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1a062-129">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1a062-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a062-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a062-130">Requirements</span></span>



| <span data-ttu-id="1a062-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a062-131">Requirement</span></span> | <span data-ttu-id="1a062-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1a062-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a062-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a062-133">Header</span></span><br/>  | <dl> <span data-ttu-id="1a062-134"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a062-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1a062-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a062-135">Library</span></span><br/> | <dl> <span data-ttu-id="1a062-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a062-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a062-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a062-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a062-138">**Interface IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="1a062-138">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="1a062-139">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="1a062-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




