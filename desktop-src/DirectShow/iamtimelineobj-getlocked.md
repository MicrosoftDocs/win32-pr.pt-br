---
description: O método getlocked recupera o estado de edição do objeto (bloqueado ou desbloqueado).
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: 'Método IAMTimelineObj:: getlocked (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 472b7dedbdbd879d4fa49fe874fb9178d0ccdee4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779535"
---
# <a name="iamtimelineobjgetlocked-method"></a><span data-ttu-id="f07e4-103">Método IAMTimelineObj:: getlocked</span><span class="sxs-lookup"><span data-stu-id="f07e4-103">IAMTimelineObj::GetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="f07e4-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f07e4-104">\[Deprecated.</span></span> <span data-ttu-id="f07e4-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f07e4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f07e4-106">O `GetLocked` método recupera o estado de edição do objeto (bloqueado ou desbloqueado).</span><span class="sxs-lookup"><span data-stu-id="f07e4-106">The `GetLocked` method retrieves the object's editing state (locked or unlocked).</span></span> <span data-ttu-id="f07e4-107">Um estado bloqueado indica que o objeto não deve ser editado; um estado desbloqueado indica que o objeto pode ser editado.</span><span class="sxs-lookup"><span data-stu-id="f07e4-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="f07e4-108">A linha do tempo não impõe o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="f07e4-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="f07e4-109">A configuração bloqueada existe apenas para a conveniência do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f07e4-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="f07e4-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f07e4-110">Syntax</span></span>


```C++
 GetLocked(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f07e4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f07e4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f07e4-112">*pVal*</span><span class="sxs-lookup"><span data-stu-id="f07e4-112">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f07e4-113">Recebe o estado de edição do objeto.</span><span class="sxs-lookup"><span data-stu-id="f07e4-113">Receives the object's editing state.</span></span> <span data-ttu-id="f07e4-114">Se o valor for **true**, o objeto será bloqueado e não deverá ser editado.</span><span class="sxs-lookup"><span data-stu-id="f07e4-114">If the value is **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="f07e4-115">Se **for false**, o objeto será desbloqueado e poderá ser editado.</span><span class="sxs-lookup"><span data-stu-id="f07e4-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f07e4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f07e4-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f07e4-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="f07e4-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f07e4-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f07e4-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f07e4-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f07e4-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f07e4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f07e4-120">Requirements</span></span>



| <span data-ttu-id="f07e4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f07e4-121">Requirement</span></span> | <span data-ttu-id="f07e4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f07e4-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f07e4-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f07e4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f07e4-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f07e4-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f07e4-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f07e4-125">Library</span></span><br/> | <dl> <span data-ttu-id="f07e4-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f07e4-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f07e4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f07e4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f07e4-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="f07e4-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="f07e4-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="f07e4-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




