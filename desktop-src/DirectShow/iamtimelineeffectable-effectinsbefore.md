---
description: O método EffectInsBefore insere um efeito no objeto no nível de prioridade especificado.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'Método IAMTimelineEffectable:: EffectInsBefore (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789947"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a><span data-ttu-id="0d2c2-103">Método IAMTimelineEffectable:: EffectInsBefore</span><span class="sxs-lookup"><span data-stu-id="0d2c2-103">IAMTimelineEffectable::EffectInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="0d2c2-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="0d2c2-104">\[Deprecated.</span></span> <span data-ttu-id="0d2c2-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d2c2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0d2c2-106">O `EffectInsBefore` método insere um efeito no objeto no nível de prioridade especificado.</span><span class="sxs-lookup"><span data-stu-id="0d2c2-106">The `EffectInsBefore` method inserts an effect into the object at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d2c2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d2c2-107">Syntax</span></span>


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="0d2c2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d2c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d2c2-109">*pFX*</span><span class="sxs-lookup"><span data-stu-id="0d2c2-109">*pFX*</span></span> 
</dt> <dd>

<span data-ttu-id="0d2c2-110">Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do efeito.</span><span class="sxs-lookup"><span data-stu-id="0d2c2-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="0d2c2-111">*Prioridade*</span><span class="sxs-lookup"><span data-stu-id="0d2c2-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="0d2c2-112">Nível de prioridade no qual inserir o efeito.</span><span class="sxs-lookup"><span data-stu-id="0d2c2-112">Priority level at which to insert the effect.</span></span> <span data-ttu-id="0d2c2-113">Use o valor – 1 para inserir o efeito no final da lista de prioridades.</span><span class="sxs-lookup"><span data-stu-id="0d2c2-113">Use the value –1 to insert the effect at the end of the priority list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d2c2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d2c2-114">Return value</span></span>

<span data-ttu-id="0d2c2-115">Retornará S \_ OK se for bem-sucedido ou E \_ NOTIMPL se o objeto não for um efeito.</span><span class="sxs-lookup"><span data-stu-id="0d2c2-115">Returns S\_OK if successful or E\_NOTIMPL if the object is not an effect.</span></span> <span data-ttu-id="0d2c2-116">Caso contrário, retorna outro valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="0d2c2-116">Otherwise, returns another **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d2c2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d2c2-117">Remarks</span></span>

<span data-ttu-id="0d2c2-118">As horas de início e de parada do efeito são recortadas dentro dos limites do intervalo de tempo do objeto, se necessário.</span><span class="sxs-lookup"><span data-stu-id="0d2c2-118">The start and stop times of the effect are clipped within the bounds of the object's time range, if necessary.</span></span> <span data-ttu-id="0d2c2-119">Se já houver um efeito no nível de prioridade especificado, todos os efeitos desse ponto em mover para baixo na lista de prioridades para liberar espaço para o novo efeito.</span><span class="sxs-lookup"><span data-stu-id="0d2c2-119">If there is already an effect at the specified priority level, all the effects from that point on move down the priority list to make room for the new effect.</span></span>

> [!Note]  
> <span data-ttu-id="0d2c2-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="0d2c2-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0d2c2-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d2c2-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0d2c2-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0d2c2-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d2c2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d2c2-123">Requirements</span></span>



| <span data-ttu-id="0d2c2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d2c2-124">Requirement</span></span> | <span data-ttu-id="0d2c2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0d2c2-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d2c2-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d2c2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0d2c2-127"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d2c2-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0d2c2-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d2c2-128">Library</span></span><br/> | <dl> <span data-ttu-id="0d2c2-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d2c2-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d2c2-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d2c2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d2c2-131">**Interface IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="0d2c2-131">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="0d2c2-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="0d2c2-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




