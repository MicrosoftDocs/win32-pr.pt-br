---
description: O \_ método Put Complication especifica o número de vezes que o padrão de apagamento é replicado verticalmente.
ms.assetid: f27e0d54-1d0f-42fe-9638-39f68b97f9c7
title: 'IDxtJpeg: método de ut_ReplicateY de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1ac5016635cb8e6f5b81b99f1ea67f0282878d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789682"
---
# <a name="idxtjpegput_replicatey-method"></a><span data-ttu-id="d7334-103">Método IDxtJpeg::p UT \_ incomplication</span><span class="sxs-lookup"><span data-stu-id="d7334-103">IDxtJpeg::put\_ReplicateY method</span></span>

> [!Note]  
> <span data-ttu-id="d7334-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d7334-104">\[Deprecated.</span></span> <span data-ttu-id="d7334-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d7334-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d7334-106">O `put_ReplicateY` método especifica o número de vezes que o padrão de apagamento é replicado verticalmente.</span><span class="sxs-lookup"><span data-stu-id="d7334-106">The `put_ReplicateY` method specifies the number of times the wipe pattern is replicated vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7334-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7334-107">Syntax</span></span>


```C++
HRESULT put_ReplicateY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="d7334-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7334-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7334-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7334-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7334-110">O número de vezes que o padrão de apagamento é replicado verticalmente.</span><span class="sxs-lookup"><span data-stu-id="d7334-110">The number of times the wipe pattern is replicated vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7334-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7334-111">Return value</span></span>

<span data-ttu-id="d7334-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d7334-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7334-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7334-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7334-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7334-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d7334-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d7334-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d7334-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d7334-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d7334-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d7334-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d7334-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7334-118">Requirements</span></span>



| <span data-ttu-id="d7334-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7334-119">Requirement</span></span> | <span data-ttu-id="d7334-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d7334-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7334-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7334-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d7334-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7334-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d7334-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7334-123">Library</span></span><br/> | <dl> <span data-ttu-id="d7334-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7334-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7334-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7334-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7334-126">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="d7334-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




