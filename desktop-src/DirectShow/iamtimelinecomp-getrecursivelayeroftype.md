---
description: O método GetRecursiveLayerOfType executa uma ordenação de profundidade das faixas virtuais contidas nessa composição e recupera a enésima faixa virtual a partir dessa ordem.
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'Método IAMTimelineComp:: GetRecursiveLayerOfType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759552"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a><span data-ttu-id="58ef2-103">Método IAMTimelineComp:: GetRecursiveLayerOfType</span><span class="sxs-lookup"><span data-stu-id="58ef2-103">IAMTimelineComp::GetRecursiveLayerOfType method</span></span>

> [!Note]  
> <span data-ttu-id="58ef2-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="58ef2-104">\[Deprecated.</span></span> <span data-ttu-id="58ef2-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="58ef2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="58ef2-106">O `GetRecursiveLayerOfType` método executa uma ordenação de profundidade das faixas virtuais contidas nessa composição e recupera a *n* º de faixa virtual dessa ordem.</span><span class="sxs-lookup"><span data-stu-id="58ef2-106">The `GetRecursiveLayerOfType` method performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ef2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58ef2-107">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="58ef2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58ef2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58ef2-109">*ppVirtualTrack* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="58ef2-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58ef2-110">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do controle virtual.</span><span class="sxs-lookup"><span data-stu-id="58ef2-110">Receives a pointer to the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="58ef2-111">*WhichLayer*</span><span class="sxs-lookup"><span data-stu-id="58ef2-111">*WhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="58ef2-112">Especifica qual faixa virtual deve ser recuperada, indexada a partir de zero.</span><span class="sxs-lookup"><span data-stu-id="58ef2-112">Specifies which virtual track to retrieve, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="58ef2-113">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="58ef2-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="58ef2-114">Membro do tipo enumerado de [**\_ \_ tipo principal da linha do tempo**](timeline-major-type.md) que especifica se as faixas devem ser incluídas na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="58ef2-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type that specifies whether to include tracks in the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58ef2-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58ef2-115">Return value</span></span>

<span data-ttu-id="58ef2-116">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="58ef2-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="58ef2-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="58ef2-117">Return code</span></span>                                                                                  | <span data-ttu-id="58ef2-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="58ef2-118">Description</span></span>                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="58ef2-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="58ef2-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="58ef2-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="58ef2-120">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="58ef2-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="58ef2-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="58ef2-122">Nenhum objeto do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="58ef2-122">No object of the specified type.</span></span><br/> |
| <dl> <span data-ttu-id="58ef2-123"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="58ef2-123"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="58ef2-124">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="58ef2-124">**NULL** pointer argument.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="58ef2-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="58ef2-125">Remarks</span></span>

<span data-ttu-id="58ef2-126">Normalmente, um aplicativo não precisará chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="58ef2-126">Typically, an application will not need to call this method.</span></span>

<span data-ttu-id="58ef2-127">Se o parâmetro de *tipo* for linha de \_ \_ tipo principal \_ faixa, a ordenação de profundidade incluirá faixas.</span><span class="sxs-lookup"><span data-stu-id="58ef2-127">If the *Type* parameter is TIMELINE\_MAJOR\_TYPE\_TRACK, the depth-first ordering includes tracks.</span></span> <span data-ttu-id="58ef2-128">Caso contrário, ele inclui apenas composições e grupos.</span><span class="sxs-lookup"><span data-stu-id="58ef2-128">If not, it includes only compositions and groups.</span></span> <span data-ttu-id="58ef2-129">O objeto em si é incluído na ordenação.</span><span class="sxs-lookup"><span data-stu-id="58ef2-129">The object itself is included in the ordering.</span></span>

<span data-ttu-id="58ef2-130">Por exemplo, no arranjo a seguir, começando da composição A, a ordenação seria B, C, F, D, E, A.</span><span class="sxs-lookup"><span data-stu-id="58ef2-130">For example, in the following arrangement, starting from Composition A, the ordering would be B, C, F, D, E, A.</span></span>

![getrecursivelayeroftype](images/composition.png)

<span data-ttu-id="58ef2-132">Se o método for executado com sucesso, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="58ef2-132">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="58ef2-133">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="58ef2-133">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="58ef2-134">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="58ef2-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="58ef2-135">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="58ef2-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="58ef2-136">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="58ef2-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58ef2-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58ef2-137">Requirements</span></span>



| <span data-ttu-id="58ef2-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="58ef2-138">Requirement</span></span> | <span data-ttu-id="58ef2-139">Valor</span><span class="sxs-lookup"><span data-stu-id="58ef2-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58ef2-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="58ef2-140">Header</span></span><br/>  | <dl> <span data-ttu-id="58ef2-141"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="58ef2-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="58ef2-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58ef2-142">Library</span></span><br/> | <dl> <span data-ttu-id="58ef2-143"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58ef2-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ef2-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="58ef2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ef2-145">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="58ef2-145">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="58ef2-146">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="58ef2-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




