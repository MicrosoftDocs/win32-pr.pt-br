---
description: O método getgroup recupera um grupo especificado.
ms.assetid: 4ff651e5-a3aa-4da9-af23-a3a2bdbf7c5b
title: 'Método IAMTimeline:: getgroup (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1241a125698cf78c1138d9264ecd8c73ff78056c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789949"
---
# <a name="iamtimelinegetgroup-method"></a><span data-ttu-id="7ef68-103">Método IAMTimeline:: getgroup</span><span class="sxs-lookup"><span data-stu-id="7ef68-103">IAMTimeline::GetGroup method</span></span>

> [!Note]  
> <span data-ttu-id="7ef68-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="7ef68-104">\[Deprecated.</span></span> <span data-ttu-id="7ef68-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7ef68-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7ef68-106">O `GetGroup` método recupera um grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="7ef68-106">The `GetGroup` method retrieves a specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ef68-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ef68-107">Syntax</span></span>


```C++
HRESULT GetGroup(
  [out] IAMTimelineObj **ppGroup,
        long           WhichGroup
);
```



## <a name="parameters"></a><span data-ttu-id="7ef68-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ef68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ef68-109">*ppGroup* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7ef68-109">*ppGroup* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef68-110">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do grupo.</span><span class="sxs-lookup"><span data-stu-id="7ef68-110">Receives a pointer to the group's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7ef68-111">*Qual o*</span><span class="sxs-lookup"><span data-stu-id="7ef68-111">*WhichGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="7ef68-112">Índice do grupo a ser recuperado, com base na ordem em que os grupos foram adicionados à linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="7ef68-112">Index of the group to retrieve, based on the order in which the groups were added to the timeline.</span></span> <span data-ttu-id="7ef68-113">O primeiro grupo adicionado à linha do tempo tem um índice de 0.</span><span class="sxs-lookup"><span data-stu-id="7ef68-113">The first group added to the timeline has an index of 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ef68-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ef68-114">Return value</span></span>

<span data-ttu-id="7ef68-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7ef68-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ef68-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ef68-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ef68-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ef68-117">Remarks</span></span>

<span data-ttu-id="7ef68-118">Se o método for executado com sucesso, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="7ef68-118">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="7ef68-119">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="7ef68-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="7ef68-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="7ef68-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ef68-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ef68-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7ef68-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7ef68-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ef68-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ef68-123">Requirements</span></span>



| <span data-ttu-id="7ef68-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ef68-124">Requirement</span></span> | <span data-ttu-id="7ef68-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7ef68-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef68-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ef68-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7ef68-127"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ef68-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7ef68-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ef68-128">Library</span></span><br/> | <dl> <span data-ttu-id="7ef68-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ef68-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ef68-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ef68-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ef68-131">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="7ef68-131">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="7ef68-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="7ef68-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




