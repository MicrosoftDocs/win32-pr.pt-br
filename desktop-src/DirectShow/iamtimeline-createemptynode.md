---
description: O método CreateEmptyNode cria um novo objeto Timeline.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: 'Método IAMTimeline:: CreateEmptyNode (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 894126bea8f40537602aa1fe8898038245215914
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757684"
---
# <a name="iamtimelinecreateemptynode-method"></a><span data-ttu-id="347d5-103">Método IAMTimeline:: CreateEmptyNode</span><span class="sxs-lookup"><span data-stu-id="347d5-103">IAMTimeline::CreateEmptyNode method</span></span>

> [!Note]  
> <span data-ttu-id="347d5-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="347d5-104">\[Deprecated.</span></span> <span data-ttu-id="347d5-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="347d5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="347d5-106">O `CreateEmptyNode` método cria um novo objeto de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="347d5-106">The `CreateEmptyNode` method creates a new timeline object.</span></span>

<span data-ttu-id="347d5-107">Use esse método para criar objetos de linha do tempo, em vez da função **CoCreateInstance** , porque esse método executa rotinas de inicialização importantes.</span><span class="sxs-lookup"><span data-stu-id="347d5-107">Use this method to create timeline objects, rather than the **CoCreateInstance** function, because this method performs important initialization routines.</span></span> <span data-ttu-id="347d5-108">Cada objeto criado por esse método dá suporte a pelo menos a interface [**IAMTimelineObj**](iamtimelineobj.md) , juntamente com outras interfaces específicas para esse tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="347d5-108">Every object created by this method supports at least the [**IAMTimelineObj**](iamtimelineobj.md) interface, along with other interfaces specific to that type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="347d5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="347d5-109">Syntax</span></span>


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="347d5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="347d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="347d5-111">*ppObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="347d5-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="347d5-112">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="347d5-112">Receives a pointer to the new object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="347d5-113">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="347d5-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="347d5-114">Membro do tipo enumerado de [**\_ \_ tipo principal da linha do tempo**](timeline-major-type.md) , especificando o tipo de objeto a ser criado.</span><span class="sxs-lookup"><span data-stu-id="347d5-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="347d5-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="347d5-115">Return value</span></span>

<span data-ttu-id="347d5-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="347d5-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="347d5-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="347d5-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="347d5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="347d5-118">Remarks</span></span>

<span data-ttu-id="347d5-119">Não adicione o novo objeto a outra instância da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="347d5-119">Do not add the new object to another timeline instance.</span></span> <span data-ttu-id="347d5-120">Cada objeto em uma linha do tempo deve ser criado por essa linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="347d5-120">Every object in a timeline must be created by that timeline.</span></span>

<span data-ttu-id="347d5-121">Se o método for executado com sucesso, a interface [**IAMTimelineObj**](iamtimelineobj.md) que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="347d5-121">If the method succeeds, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="347d5-122">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="347d5-122">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="347d5-123">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="347d5-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="347d5-124">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="347d5-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="347d5-125">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="347d5-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="347d5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="347d5-126">Requirements</span></span>



| <span data-ttu-id="347d5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="347d5-127">Requirement</span></span> | <span data-ttu-id="347d5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="347d5-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="347d5-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="347d5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="347d5-130"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="347d5-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="347d5-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="347d5-131">Library</span></span><br/> | <dl> <span data-ttu-id="347d5-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="347d5-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="347d5-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="347d5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="347d5-134">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="347d5-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="347d5-135">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="347d5-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




