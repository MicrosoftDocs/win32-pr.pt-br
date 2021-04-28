---
description: 'Método IXml2Dex:: WriteXMLPart-não implementado.'
ms.assetid: d0fc571f-79f5-448a-8082-6e5f7f48118f
title: 'Método IXml2Dex:: WriteXMLPart'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 957fa74f09a79f94e2e0feb35c418a711c91c1b0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084354"
---
# <a name="ixml2dexwritexmlpart-method"></a><span data-ttu-id="43d5b-103">Método IXml2Dex:: WriteXMLPart</span><span class="sxs-lookup"><span data-stu-id="43d5b-103">IXml2Dex::WriteXMLPart method</span></span>

> [!Note]  
> <span data-ttu-id="43d5b-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="43d5b-104">\[Deprecated.</span></span> <span data-ttu-id="43d5b-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="43d5b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="43d5b-106">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="43d5b-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d5b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43d5b-107">Syntax</span></span>


```C++
HRESULT WriteXMLPart(
   IUnknown *pTimeline,
   double   dStart,
   double   dEnd,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="43d5b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43d5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43d5b-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="43d5b-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="43d5b-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="43d5b-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="43d5b-111">*dStart*</span><span class="sxs-lookup"><span data-stu-id="43d5b-111">*dStart*</span></span> 
</dt> <dd>

<span data-ttu-id="43d5b-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="43d5b-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="43d5b-113">*dEnd*</span><span class="sxs-lookup"><span data-stu-id="43d5b-113">*dEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="43d5b-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="43d5b-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="43d5b-115">*FileName*</span><span class="sxs-lookup"><span data-stu-id="43d5b-115">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="43d5b-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="43d5b-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43d5b-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="43d5b-117">Return value</span></span>

<span data-ttu-id="43d5b-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="43d5b-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43d5b-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43d5b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="43d5b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="43d5b-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="43d5b-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="43d5b-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="43d5b-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="43d5b-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="43d5b-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="43d5b-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="43d5b-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="43d5b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d5b-125">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="43d5b-125">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> </dl>

 

 



