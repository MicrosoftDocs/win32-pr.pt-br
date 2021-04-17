---
description: O método MakeIdentityPalette tenta tornar uma paleta de \# identidade &0034;, &\# 0034; definida como uma que é mapeada diretamente para a paleta selecionada no dispositivo de vídeo.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Método CImagePalette. MakeIdentityPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e105652108e74907375408f0bd8946c69194202
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748445"
---
# <a name="cimagepalettemakeidentitypalette-method"></a><span data-ttu-id="0afc1-103">Método CImagePalette. MakeIdentityPalette</span><span class="sxs-lookup"><span data-stu-id="0afc1-103">CImagePalette.MakeIdentityPalette method</span></span>

<span data-ttu-id="0afc1-104">O `MakeIdentityPalette` método tenta criar uma "paleta de identidade", definida como uma que é mapeada diretamente para a paleta selecionada no dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0afc1-104">The `MakeIdentityPalette` method attempts to make an "identity palette," defined as one that maps directly to the palette selected in the display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0afc1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0afc1-105">Syntax</span></span>


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="0afc1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0afc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0afc1-107">*pEntry*</span><span class="sxs-lookup"><span data-stu-id="0afc1-107">*pEntry*</span></span> 
</dt> <dd>

<span data-ttu-id="0afc1-108">Ponteiro para uma matriz de entradas de paleta.</span><span class="sxs-lookup"><span data-stu-id="0afc1-108">Pointer to an array of palette entries.</span></span>

</dd> <dt>

<span data-ttu-id="0afc1-109">*iColours*</span><span class="sxs-lookup"><span data-stu-id="0afc1-109">*iColours*</span></span> 
</dt> <dd>

<span data-ttu-id="0afc1-110">Número de entradas de paleta em *pentry*.</span><span class="sxs-lookup"><span data-stu-id="0afc1-110">Number of palette entries in *pEntry*.</span></span>

</dd> <dt>

<span data-ttu-id="0afc1-111">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="0afc1-111">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="0afc1-112">Ponteiro para uma cadeia de caracteres que contém o nome do dispositivo de vídeo, conforme retornado pela função **EnumDisplayDevices** do GDI.</span><span class="sxs-lookup"><span data-stu-id="0afc1-112">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="0afc1-113">Para usar o dispositivo de vídeo principal, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0afc1-113">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0afc1-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0afc1-114">Return value</span></span>

<span data-ttu-id="0afc1-115">Retornará S \_ OK se for bem-sucedido ou S \_ false se for malsucedido.</span><span class="sxs-lookup"><span data-stu-id="0afc1-115">Returns S\_OK if successful or S\_FALSE if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0afc1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0afc1-116">Remarks</span></span>

<span data-ttu-id="0afc1-117">Esse método compara as entradas reservadas na paleta do sistema com as entradas correspondentes na matriz *pentry* .</span><span class="sxs-lookup"><span data-stu-id="0afc1-117">This method compares the reserved entries in the system palette against the corresponding entries in the *pEntry* array.</span></span> <span data-ttu-id="0afc1-118">Se eles corresponderem exatamente, o método definirá o \_ sinalizador de DESrecolhimento do PC nas entradas de paleta restantes (não reservadas) em *pentry*.</span><span class="sxs-lookup"><span data-stu-id="0afc1-118">If they match exactly, the method sets the PC\_NOCOLLAPSE flag in the remaining (non-reserved) palette entries in *pEntry*.</span></span> <span data-ttu-id="0afc1-119">Esse sinalizador impede que o GDI tente mapear entradas de paleta lógica para entradas da paleta do sistema.</span><span class="sxs-lookup"><span data-stu-id="0afc1-119">This flag prevents GDI from trying map logical palette entries to system palette entries.</span></span>

<span data-ttu-id="0afc1-120">O método [**CImagePalette:: MakePalette**](cimagepalette-makepalette.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="0afc1-120">The [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0afc1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0afc1-121">Requirements</span></span>



| <span data-ttu-id="0afc1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0afc1-122">Requirement</span></span> | <span data-ttu-id="0afc1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0afc1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0afc1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0afc1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0afc1-125"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0afc1-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0afc1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0afc1-126">Library</span></span><br/> | <dl> <span data-ttu-id="0afc1-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0afc1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0afc1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0afc1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0afc1-129">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="0afc1-129">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




