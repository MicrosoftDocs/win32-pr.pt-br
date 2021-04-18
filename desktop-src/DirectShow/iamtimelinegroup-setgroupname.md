---
description: O método setgroupname define o nome definido pelo aplicativo do grupo.
ms.assetid: e1d8a91b-d5b9-42a4-9b98-582e1a57ac51
title: 'Método IAMTimelineGroup:: setgroupname (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 327bf0384ce484353ac41c069ddf580c674b0b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812985"
---
# <a name="iamtimelinegroupsetgroupname-method"></a><span data-ttu-id="61fea-103">Método IAMTimelineGroup:: setgroupname</span><span class="sxs-lookup"><span data-stu-id="61fea-103">IAMTimelineGroup::SetGroupName method</span></span>

> [!Note]  
> <span data-ttu-id="61fea-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="61fea-104">\[Deprecated.</span></span> <span data-ttu-id="61fea-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="61fea-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="61fea-106">O `SetGroupName` método define o nome definido pelo aplicativo do grupo.</span><span class="sxs-lookup"><span data-stu-id="61fea-106">The `SetGroupName` method sets the application-defined name of the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="61fea-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61fea-107">Syntax</span></span>


```C++
HRESULT SetGroupName(
   BSTR pGroupName
);
```



## <a name="parameters"></a><span data-ttu-id="61fea-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61fea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61fea-109">*pGroupName*</span><span class="sxs-lookup"><span data-stu-id="61fea-109">*pGroupName*</span></span> 
</dt> <dd>

<span data-ttu-id="61fea-110">**BSTR** que especifica o nome do grupo.</span><span class="sxs-lookup"><span data-stu-id="61fea-110">**BSTR** that specifies the name of the group.</span></span> <span data-ttu-id="61fea-111">O comprimento máximo do nome é de 256 caracteres, incluindo o terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="61fea-111">The maximum length of the name is 256 characters, incuding the null terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61fea-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61fea-112">Return value</span></span>

<span data-ttu-id="61fea-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="61fea-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="61fea-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="61fea-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="61fea-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="61fea-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="61fea-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="61fea-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="61fea-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="61fea-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="61fea-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="61fea-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="61fea-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61fea-119">Requirements</span></span>



| <span data-ttu-id="61fea-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="61fea-120">Requirement</span></span> | <span data-ttu-id="61fea-121">Valor</span><span class="sxs-lookup"><span data-stu-id="61fea-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61fea-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61fea-122">Header</span></span><br/>  | <dl> <span data-ttu-id="61fea-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="61fea-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="61fea-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61fea-124">Library</span></span><br/> | <dl> <span data-ttu-id="61fea-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61fea-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61fea-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="61fea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61fea-127">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="61fea-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="61fea-128">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="61fea-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




