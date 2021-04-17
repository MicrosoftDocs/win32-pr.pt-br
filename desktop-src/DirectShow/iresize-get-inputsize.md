---
description: O \_ método Get Incolocate retorna o tamanho de entrada atual do filtro de redimensionador.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'Método IResize:: get_InputSize (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fab61edf6dc4469f06437483172161fbbe77e76d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812773"
---
# <a name="iresizeget_inputsize-method"></a><span data-ttu-id="e978a-103">Método IResize:: get \_ Incolocate</span><span class="sxs-lookup"><span data-stu-id="e978a-103">IResize::get\_InputSize method</span></span>

> [!Note]  
> <span data-ttu-id="e978a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="e978a-104">\[Deprecated.</span></span> <span data-ttu-id="e978a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e978a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e978a-106">O `get_InputSize` método retorna o tamanho de entrada atual do filtro de redimensionador.</span><span class="sxs-lookup"><span data-stu-id="e978a-106">The `get_InputSize` method returns the resizer filter's current input size.</span></span>

## <a name="syntax"></a><span data-ttu-id="e978a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e978a-107">Syntax</span></span>


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a><span data-ttu-id="e978a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e978a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e978a-109">*piHeight* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e978a-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e978a-110">Recebe a altura do vídeo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e978a-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e978a-111">*piWidth* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e978a-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e978a-112">Recebe a largura do vídeo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e978a-112">Receives the video width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e978a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e978a-113">Return value</span></span>

<span data-ttu-id="e978a-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e978a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e978a-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e978a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e978a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e978a-116">Remarks</span></span>

<span data-ttu-id="e978a-117">Se o pino de entrada do filtro não estiver conectado, retorne um código de erro.</span><span class="sxs-lookup"><span data-stu-id="e978a-117">If the filter's input pin is not connected, return an error code.</span></span> <span data-ttu-id="e978a-118">Caso contrário, retorne a largura e a altura do vídeo, conforme especificado pelo tipo de mídia do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="e978a-118">Otherwise, return the width and height of the video, as specified by the input pin's media type.</span></span>

> [!Note]  
> <span data-ttu-id="e978a-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="e978a-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e978a-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e978a-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e978a-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e978a-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e978a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e978a-122">Requirements</span></span>



| <span data-ttu-id="e978a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e978a-123">Requirement</span></span> | <span data-ttu-id="e978a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e978a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e978a-125">Versão</span><span class="sxs-lookup"><span data-stu-id="e978a-125">Version</span></span><br/> | <span data-ttu-id="e978a-126">DirectX 9,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e978a-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="e978a-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e978a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e978a-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e978a-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e978a-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e978a-129">Library</span></span><br/> | <dl> <span data-ttu-id="e978a-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e978a-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e978a-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e978a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e978a-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="e978a-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="e978a-133">**Interface IResize**</span><span class="sxs-lookup"><span data-stu-id="e978a-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




