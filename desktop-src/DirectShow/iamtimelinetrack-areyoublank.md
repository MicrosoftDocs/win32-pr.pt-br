---
description: O método AreYouBlank determina se a faixa está em branco (não contém nenhum objeto de origem).
ms.assetid: 05d02753-6e40-4307-9445-c3cbc835f75e
title: 'Método IAMTimelineTrack:: AreYouBlank (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.AreYouBlank
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 289fac360f989504d3eb5108f8c2388ac4a06b09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779848"
---
# <a name="iamtimelinetrackareyoublank-method"></a><span data-ttu-id="5547e-103">Método IAMTimelineTrack:: AreYouBlank</span><span class="sxs-lookup"><span data-stu-id="5547e-103">IAMTimelineTrack::AreYouBlank method</span></span>

> [!Note]  
> <span data-ttu-id="5547e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="5547e-104">\[Deprecated.</span></span> <span data-ttu-id="5547e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5547e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5547e-106">O `AreYouBlank` método determina se a faixa está em branco (não contém nenhum objeto de origem).</span><span class="sxs-lookup"><span data-stu-id="5547e-106">The `AreYouBlank` method determines whether the track is blank (contains no source objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="5547e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5547e-107">Syntax</span></span>


```C++
HRESULT AreYouBlank(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5547e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5547e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5547e-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="5547e-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="5547e-110">Recebe um valor booliano que especifica se a faixa está em branco.</span><span class="sxs-lookup"><span data-stu-id="5547e-110">Receives a Boolean value specifying whether the track is blank.</span></span> <span data-ttu-id="5547e-111">Se o valor for **true**, a faixa ficará em branco e não conterá nenhum objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="5547e-111">If the value is **TRUE**, the track is blank and contains no source objects.</span></span> <span data-ttu-id="5547e-112">Se for **false**, a faixa não ficará em branco.</span><span class="sxs-lookup"><span data-stu-id="5547e-112">If **FALSE**, the track is not blank.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5547e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5547e-113">Return value</span></span>

<span data-ttu-id="5547e-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5547e-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5547e-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5547e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5547e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5547e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5547e-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="5547e-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5547e-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5547e-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5547e-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5547e-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5547e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5547e-120">Requirements</span></span>



| <span data-ttu-id="5547e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5547e-121">Requirement</span></span> | <span data-ttu-id="5547e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5547e-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5547e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5547e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5547e-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5547e-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5547e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5547e-125">Library</span></span><br/> | <dl> <span data-ttu-id="5547e-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5547e-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5547e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5547e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5547e-128">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="5547e-128">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="5547e-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="5547e-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




