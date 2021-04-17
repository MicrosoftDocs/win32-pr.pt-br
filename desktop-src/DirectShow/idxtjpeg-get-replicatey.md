---
description: O \_ método obter Complication recupera o número de vezes que o padrão de apagamento é replicado verticalmente.
ms.assetid: 347e1ffa-bb39-4980-b8af-5806a23d1334
title: 'Método IDxtJpeg:: get_ReplicateY (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ae5c68d153b64783f84a6c4c4a8ba7f5d5f0f24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789938"
---
# <a name="idxtjpegget_replicatey-method"></a><span data-ttu-id="f05eb-103">Método de complicação IDxtJpeg:: get \_</span><span class="sxs-lookup"><span data-stu-id="f05eb-103">IDxtJpeg::get\_ReplicateY method</span></span>

> [!Note]  
> <span data-ttu-id="f05eb-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f05eb-104">\[Deprecated.</span></span> <span data-ttu-id="f05eb-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f05eb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f05eb-106">O `get_ReplicateY` método recupera o número de vezes que o padrão de apagamento é replicado verticalmente.</span><span class="sxs-lookup"><span data-stu-id="f05eb-106">The `get_ReplicateY` method retrieves the number of times the wipe pattern is replicated vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="f05eb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f05eb-107">Syntax</span></span>


```C++
HRESULT get_ReplicateY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f05eb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f05eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f05eb-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f05eb-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f05eb-110">Recebe o número de vezes que o padrão de apagamento é replicado verticalmente.</span><span class="sxs-lookup"><span data-stu-id="f05eb-110">Receives the number of times the wipe pattern is replicated vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f05eb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f05eb-111">Return value</span></span>

<span data-ttu-id="f05eb-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f05eb-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f05eb-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f05eb-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f05eb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f05eb-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f05eb-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="f05eb-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f05eb-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f05eb-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f05eb-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f05eb-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f05eb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f05eb-118">Requirements</span></span>



| <span data-ttu-id="f05eb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f05eb-119">Requirement</span></span> | <span data-ttu-id="f05eb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f05eb-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f05eb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f05eb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f05eb-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f05eb-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f05eb-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f05eb-123">Library</span></span><br/> | <dl> <span data-ttu-id="f05eb-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f05eb-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f05eb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f05eb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f05eb-126">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="f05eb-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




