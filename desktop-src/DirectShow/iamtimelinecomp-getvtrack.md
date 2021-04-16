---
description: O método GetVTrack recupera a faixa virtual na prioridade especificada.
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: 'Método IAMTimelineComp:: GetVTrack (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 06c205f700cbdb98fdc5f45bdd2ca7727e2456f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758684"
---
# <a name="iamtimelinecompgetvtrack-method"></a><span data-ttu-id="e1977-103">Método IAMTimelineComp:: GetVTrack</span><span class="sxs-lookup"><span data-stu-id="e1977-103">IAMTimelineComp::GetVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="e1977-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="e1977-104">\[Deprecated.</span></span> <span data-ttu-id="e1977-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e1977-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e1977-106">O `GetVTrack` método recupera a faixa virtual na prioridade especificada.</span><span class="sxs-lookup"><span data-stu-id="e1977-106">The `GetVTrack` method retrieves the virtual track at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1977-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1977-107">Syntax</span></span>


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="e1977-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1977-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1977-109">*ppVirtualTrack* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e1977-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1977-110">Recebe a interface [**IAMTimelineObj**](iamtimelineobj.md) do controle virtual.</span><span class="sxs-lookup"><span data-stu-id="e1977-110">Receives the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e1977-111">*Onde*</span><span class="sxs-lookup"><span data-stu-id="e1977-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="e1977-112">Prioridade da faixa virtual a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="e1977-112">Priority of the virtual track to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1977-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1977-113">Return value</span></span>

<span data-ttu-id="e1977-114">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="e1977-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e1977-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e1977-115">Return code</span></span>                                                                                  | <span data-ttu-id="e1977-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1977-116">Description</span></span>                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="e1977-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e1977-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e1977-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="e1977-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="e1977-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e1977-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e1977-120">Nenhuma faixa virtual com a prioridade especificada.</span><span class="sxs-lookup"><span data-stu-id="e1977-120">No virtual track with the specified priority.</span></span><br/> |
| <dl> <span data-ttu-id="e1977-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="e1977-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="e1977-122">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="e1977-122">**NULL** pointer argument.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e1977-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1977-123">Remarks</span></span>

<span data-ttu-id="e1977-124">Se o método for executado com sucesso, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="e1977-124">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="e1977-125">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="e1977-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="e1977-126">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="e1977-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e1977-127">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e1977-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e1977-128">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e1977-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e1977-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1977-129">Requirements</span></span>



| <span data-ttu-id="e1977-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1977-130">Requirement</span></span> | <span data-ttu-id="e1977-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e1977-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1977-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1977-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e1977-133"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1977-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e1977-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1977-134">Library</span></span><br/> | <dl> <span data-ttu-id="e1977-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1977-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1977-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1977-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1977-137">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="e1977-137">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="e1977-138">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="e1977-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




