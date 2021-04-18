---
description: O método setlocked define o estado de edição do objeto como bloqueado ou desbloqueado.
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: 'Método IAMTimelineObj:: setlocked (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8707aa86b651553dde2f9f9b57c84169a9969b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778473"
---
# <a name="iamtimelineobjsetlocked-method"></a><span data-ttu-id="81602-103">Método IAMTimelineObj:: setlocked</span><span class="sxs-lookup"><span data-stu-id="81602-103">IAMTimelineObj::SetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="81602-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="81602-104">\[Deprecated.</span></span> <span data-ttu-id="81602-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="81602-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="81602-106">O `SetLocked` método define o estado de edição do objeto como bloqueado ou desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="81602-106">The `SetLocked` method sets the object's editing state to locked or unlocked.</span></span>

<span data-ttu-id="81602-107">Um estado bloqueado indica que o objeto não deve ser editado; um estado desbloqueado indica que o objeto pode ser editado.</span><span class="sxs-lookup"><span data-stu-id="81602-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="81602-108">A linha do tempo não impõe o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="81602-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="81602-109">A configuração bloqueada existe apenas para a conveniência do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81602-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="81602-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81602-110">Syntax</span></span>


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="81602-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81602-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81602-112">*newVal*</span><span class="sxs-lookup"><span data-stu-id="81602-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="81602-113">Valor booliano que especifica o estado de edição do objeto.</span><span class="sxs-lookup"><span data-stu-id="81602-113">Boolean value that specifies the object's editing state.</span></span> <span data-ttu-id="81602-114">Se **for true**, o objeto será bloqueado e não deverá ser editado.</span><span class="sxs-lookup"><span data-stu-id="81602-114">If **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="81602-115">Se **for false**, o objeto será desbloqueado e poderá ser editado.</span><span class="sxs-lookup"><span data-stu-id="81602-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81602-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81602-116">Return value</span></span>

<span data-ttu-id="81602-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="81602-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="81602-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81602-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="81602-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="81602-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="81602-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="81602-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="81602-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="81602-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="81602-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="81602-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81602-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81602-123">Requirements</span></span>



| <span data-ttu-id="81602-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="81602-124">Requirement</span></span> | <span data-ttu-id="81602-125">Valor</span><span class="sxs-lookup"><span data-stu-id="81602-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81602-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81602-126">Header</span></span><br/>  | <dl> <span data-ttu-id="81602-127"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="81602-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="81602-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81602-128">Library</span></span><br/> | <dl> <span data-ttu-id="81602-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81602-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81602-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="81602-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81602-131">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="81602-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="81602-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="81602-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




