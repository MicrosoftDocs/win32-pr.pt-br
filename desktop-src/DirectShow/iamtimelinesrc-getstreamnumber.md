---
description: O método GetStreamNumber recupera o número de fluxo atual para o objeto de origem.
ms.assetid: c9c0c9f7-2716-436d-902c-f2255bedaffb
title: 'Método IAMTimelineSrc:: GetStreamNumber (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d6fc9387499f675dd011dbceecbaf1aecdd287ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785491"
---
# <a name="iamtimelinesrcgetstreamnumber-method"></a><span data-ttu-id="4c635-103">Método IAMTimelineSrc:: GetStreamNumber</span><span class="sxs-lookup"><span data-stu-id="4c635-103">IAMTimelineSrc::GetStreamNumber method</span></span>

> [!Note]  
> <span data-ttu-id="4c635-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="4c635-104">\[Deprecated.</span></span> <span data-ttu-id="4c635-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4c635-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4c635-106">O `GetStreamNumber` método recupera o número de fluxo atual para o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="4c635-106">The `GetStreamNumber` method retrieves the current stream number for the source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c635-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c635-107">Syntax</span></span>


```C++
HRESULT GetStreamNumber(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4c635-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c635-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c635-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="4c635-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="4c635-110">Recebe o número do fluxo.</span><span class="sxs-lookup"><span data-stu-id="4c635-110">Receives the stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c635-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c635-111">Return value</span></span>

<span data-ttu-id="4c635-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4c635-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c635-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c635-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c635-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c635-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c635-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="4c635-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4c635-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c635-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4c635-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4c635-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c635-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c635-118">Requirements</span></span>



| <span data-ttu-id="4c635-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c635-119">Requirement</span></span> | <span data-ttu-id="4c635-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4c635-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c635-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c635-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4c635-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c635-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4c635-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c635-123">Library</span></span><br/> | <dl> <span data-ttu-id="4c635-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c635-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c635-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c635-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c635-126">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="4c635-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="4c635-127">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="4c635-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




