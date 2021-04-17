---
description: O \_ método Get ReplicateX recupera o número de vezes que o padrão de apagamento é replicado horizontalmente.
ms.assetid: 669a3bde-af8b-4d31-b914-41b71c95de1c
title: 'Método IDxtJpeg:: get_ReplicateX (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ReplicateX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8855f819cb00d46297220c41deb6b81d6150e0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812822"
---
# <a name="idxtjpegget_replicatex-method"></a><span data-ttu-id="8ee10-103">Método IDxtJpeg:: get \_ ReplicateX</span><span class="sxs-lookup"><span data-stu-id="8ee10-103">IDxtJpeg::get\_ReplicateX method</span></span>

> [!Note]  
> <span data-ttu-id="8ee10-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="8ee10-104">\[Deprecated.</span></span> <span data-ttu-id="8ee10-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8ee10-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8ee10-106">O `get_ReplicateX` método recupera o número de vezes que o padrão de apagamento é replicado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="8ee10-106">The `get_ReplicateX` method retrieves the number of times the wipe pattern is replicated horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee10-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ee10-107">Syntax</span></span>


```C++
HRESULT get_ReplicateX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8ee10-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ee10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ee10-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8ee10-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee10-110">Recebe o número de vezes que o padrão de apagamento é replicado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="8ee10-110">Receives the number of times the wipe pattern is replicated horizontally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ee10-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ee10-111">Return value</span></span>

<span data-ttu-id="8ee10-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8ee10-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ee10-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ee10-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ee10-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ee10-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8ee10-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="8ee10-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8ee10-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8ee10-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8ee10-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8ee10-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ee10-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ee10-118">Requirements</span></span>



| <span data-ttu-id="8ee10-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ee10-119">Requirement</span></span> | <span data-ttu-id="8ee10-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8ee10-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee10-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ee10-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8ee10-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee10-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8ee10-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ee10-123">Library</span></span><br/> | <dl> <span data-ttu-id="8ee10-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ee10-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ee10-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ee10-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee10-126">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="8ee10-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




