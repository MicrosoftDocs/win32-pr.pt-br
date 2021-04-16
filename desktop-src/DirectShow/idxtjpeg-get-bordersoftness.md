---
description: O \_ método Get BorderSoftness recupera a largura da região borrada ao contrário das bordas do padrão de apagamento.
ms.assetid: f5648cce-e44c-4ed6-8254-6511cd600629
title: 'Método IDxtJpeg:: get_BorderSoftness (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderSoftness
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 968dbef4a87a7b88e16321693350d35d08225c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779530"
---
# <a name="idxtjpegget_bordersoftness-method"></a><span data-ttu-id="1cbab-103">Método IDxtJpeg:: get \_ BorderSoftness</span><span class="sxs-lookup"><span data-stu-id="1cbab-103">IDxtJpeg::get\_BorderSoftness method</span></span>

> [!Note]  
> <span data-ttu-id="1cbab-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="1cbab-104">\[Deprecated.</span></span> <span data-ttu-id="1cbab-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1cbab-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1cbab-106">O `get_BorderSoftness` método recupera a largura da região borrada em volta das bordas do padrão de apagamento.</span><span class="sxs-lookup"><span data-stu-id="1cbab-106">The `get_BorderSoftness` method retrieves the width of the blurry region around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cbab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cbab-107">Syntax</span></span>


```C++
HRESULT get_BorderSoftness(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1cbab-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cbab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cbab-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1cbab-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1cbab-110">Recebe a largura da região borrada, em pixels.</span><span class="sxs-lookup"><span data-stu-id="1cbab-110">Receives the width of the blurry region, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cbab-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1cbab-111">Return value</span></span>

<span data-ttu-id="1cbab-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1cbab-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1cbab-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1cbab-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cbab-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cbab-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1cbab-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="1cbab-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1cbab-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1cbab-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1cbab-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1cbab-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1cbab-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cbab-118">Requirements</span></span>



| <span data-ttu-id="1cbab-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cbab-119">Requirement</span></span> | <span data-ttu-id="1cbab-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1cbab-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbab-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1cbab-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1cbab-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cbab-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1cbab-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1cbab-123">Library</span></span><br/> | <dl> <span data-ttu-id="1cbab-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cbab-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cbab-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cbab-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cbab-126">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="1cbab-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




