---
description: O \_ método Put ReplicateX especifica o número de vezes que o padrão de apagamento é replicado horizontalmente.
ms.assetid: 8baa641c-c063-4c22-8b00-3559c173d627
title: 'IDxtJpeg: método de ut_ReplicateX de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08d892619fe1e6f8222b40d45e634a350e4e9b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768631"
---
# <a name="idxtjpegput_replicatex-method"></a><span data-ttu-id="d6296-103">IDxtJpeg: método UT \_ ReplicateX:p</span><span class="sxs-lookup"><span data-stu-id="d6296-103">IDxtJpeg::put\_ReplicateX method</span></span>

> [!Note]  
> <span data-ttu-id="d6296-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d6296-104">\[Deprecated.</span></span> <span data-ttu-id="d6296-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d6296-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d6296-106">O `put_ReplicateX` método especifica o número de vezes que o padrão de apagamento é replicado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="d6296-106">The `put_ReplicateX` method specifies the number of times the wipe pattern is replicated horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6296-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6296-107">Syntax</span></span>


```C++
HRESULT put_ReplicateX(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="d6296-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6296-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6296-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6296-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6296-110">O número de vezes que o padrão de apagamento é replicado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="d6296-110">The number of times the wipe pattern is replicated horizontally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6296-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6296-111">Return value</span></span>

<span data-ttu-id="d6296-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d6296-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6296-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6296-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6296-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6296-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d6296-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d6296-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d6296-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d6296-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d6296-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d6296-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d6296-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6296-118">Requirements</span></span>



| <span data-ttu-id="d6296-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6296-119">Requirement</span></span> | <span data-ttu-id="d6296-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d6296-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6296-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6296-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d6296-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6296-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d6296-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6296-123">Library</span></span><br/> | <dl> <span data-ttu-id="d6296-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6296-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6296-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6296-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6296-126">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="d6296-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




