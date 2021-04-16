---
description: O método UpdateColourTable atualiza a tabela de cores com uma nova paleta.
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: Método CDrawImage. UpdateColourTable (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UpdateColourTable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcffdf9e7deaaac5a01f6559ee557c978fcda88f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758859"
---
# <a name="cdrawimageupdatecolourtable-method"></a><span data-ttu-id="f0403-103">Método CDrawImage. UpdateColourTable</span><span class="sxs-lookup"><span data-stu-id="f0403-103">CDrawImage.UpdateColourTable method</span></span>

<span data-ttu-id="f0403-104">O `UpdateColourTable` método atualiza a tabela de cores com uma nova paleta.</span><span class="sxs-lookup"><span data-stu-id="f0403-104">The `UpdateColourTable` method updates the color table with a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0403-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0403-105">Syntax</span></span>


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a><span data-ttu-id="f0403-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0403-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0403-107">*HDC*</span><span class="sxs-lookup"><span data-stu-id="f0403-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="f0403-108">Contexto do dispositivo que contém a imagem.</span><span class="sxs-lookup"><span data-stu-id="f0403-108">Device context containing the image.</span></span>

</dd> <dt>

<span data-ttu-id="f0403-109">*pbmi*</span><span class="sxs-lookup"><span data-stu-id="f0403-109">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="f0403-110">Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que contém a nova paleta.</span><span class="sxs-lookup"><span data-stu-id="f0403-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure containing the new palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0403-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0403-111">Return value</span></span>

<span data-ttu-id="f0403-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f0403-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0403-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0403-113">Requirements</span></span>



| <span data-ttu-id="f0403-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0403-114">Requirement</span></span> | <span data-ttu-id="f0403-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f0403-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0403-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0403-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f0403-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0403-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f0403-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0403-118">Library</span></span><br/> | <dl> <span data-ttu-id="f0403-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f0403-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0403-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0403-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0403-121">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="f0403-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




