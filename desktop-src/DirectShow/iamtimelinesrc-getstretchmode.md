---
description: O método getstretchmode recupera o modo Stretch. O modo de ampliação determina como uma fonte de vídeo será renderizada se seu tamanho não corresponder às dimensões de saída.
ms.assetid: d9a3d283-edb5-40be-b877-69cb23462afa
title: 'Método IAMTimelineSrc:: getstretchmode (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f10552ac67c50e8656f303fd524bdad2cd07823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810224"
---
# <a name="iamtimelinesrcgetstretchmode-method"></a><span data-ttu-id="d3f6a-104">Método IAMTimelineSrc:: getstretchmode</span><span class="sxs-lookup"><span data-stu-id="d3f6a-104">IAMTimelineSrc::GetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="d3f6a-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d3f6a-105">\[Deprecated.</span></span> <span data-ttu-id="d3f6a-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d3f6a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d3f6a-107">O `GetStretchMode` método recupera o modo Stretch.</span><span class="sxs-lookup"><span data-stu-id="d3f6a-107">The `GetStretchMode` method retrieves the stretch mode.</span></span> <span data-ttu-id="d3f6a-108">O modo de ampliação determina como uma fonte de vídeo será renderizada se seu tamanho não corresponder às dimensões de saída.</span><span class="sxs-lookup"><span data-stu-id="d3f6a-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f6a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3f6a-109">Syntax</span></span>


```C++
HRESULT GetStretchMode(
   int *pnStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="d3f6a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3f6a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3f6a-111">*pnStretchMode*</span><span class="sxs-lookup"><span data-stu-id="d3f6a-111">*pnStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="d3f6a-112">Recebe um sinalizador que indica o modo de Stretch atual.</span><span class="sxs-lookup"><span data-stu-id="d3f6a-112">Receives a flag indicating the current stretch mode.</span></span> <span data-ttu-id="d3f6a-113">Para obter uma lista de valores possíveis, consulte [**redimensionar sinalizadores**](resize-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d3f6a-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3f6a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3f6a-114">Return value</span></span>

<span data-ttu-id="d3f6a-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d3f6a-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3f6a-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3f6a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3f6a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3f6a-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d3f6a-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d3f6a-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d3f6a-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d3f6a-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d3f6a-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d3f6a-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d3f6a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3f6a-121">Requirements</span></span>



| <span data-ttu-id="d3f6a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3f6a-122">Requirement</span></span> | <span data-ttu-id="d3f6a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d3f6a-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f6a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3f6a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d3f6a-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3f6a-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d3f6a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3f6a-126">Library</span></span><br/> | <dl> <span data-ttu-id="d3f6a-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3f6a-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3f6a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3f6a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f6a-129">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="d3f6a-129">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="d3f6a-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="d3f6a-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




