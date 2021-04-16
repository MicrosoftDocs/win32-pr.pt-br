---
description: O \_ método Get BorderColor recupera a cor da borda ao contrário das bordas do padrão de apagamento.
ms.assetid: 9d36cc49-c174-4b93-a030-ca8d2890c624
title: 'Método IDxtJpeg:: get_BorderColor (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f37c37865caf76839733ada376ec637747977ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768634"
---
# <a name="idxtjpegget_bordercolor-method"></a><span data-ttu-id="53ccc-103">Método IDxtJpeg:: get \_ BorderColor</span><span class="sxs-lookup"><span data-stu-id="53ccc-103">IDxtJpeg::get\_BorderColor method</span></span>

> [!Note]  
> <span data-ttu-id="53ccc-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="53ccc-104">\[Deprecated.</span></span> <span data-ttu-id="53ccc-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53ccc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="53ccc-106">O `get_BorderColor` método recupera a cor da borda em torno das bordas do padrão de apagamento.</span><span class="sxs-lookup"><span data-stu-id="53ccc-106">The `get_BorderColor` method retrieves the color of the border around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="53ccc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53ccc-107">Syntax</span></span>


```C++
HRESULT get_BorderColor(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="53ccc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53ccc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53ccc-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="53ccc-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="53ccc-110">Recebe a cor.</span><span class="sxs-lookup"><span data-stu-id="53ccc-110">Receives the color.</span></span> <span data-ttu-id="53ccc-111">O valor retornado é um número hexadecimal com o formato 0xRRGGBB, em que RR é o valor vermelho, GG é o valor verde e BB é o valor azul.</span><span class="sxs-lookup"><span data-stu-id="53ccc-111">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53ccc-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53ccc-112">Return value</span></span>

<span data-ttu-id="53ccc-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="53ccc-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53ccc-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53ccc-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="53ccc-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="53ccc-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="53ccc-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="53ccc-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="53ccc-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="53ccc-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="53ccc-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="53ccc-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53ccc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53ccc-119">Requirements</span></span>



| <span data-ttu-id="53ccc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="53ccc-120">Requirement</span></span> | <span data-ttu-id="53ccc-121">Valor</span><span class="sxs-lookup"><span data-stu-id="53ccc-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53ccc-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53ccc-122">Header</span></span><br/>  | <dl> <span data-ttu-id="53ccc-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="53ccc-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="53ccc-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53ccc-124">Library</span></span><br/> | <dl> <span data-ttu-id="53ccc-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53ccc-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53ccc-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="53ccc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53ccc-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="53ccc-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




