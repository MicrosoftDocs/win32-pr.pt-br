---
description: O método ShouldUpdate determina se é necessário criar uma nova paleta.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Método CImagePalette. ShouldUpdate (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756599"
---
# <a name="cimagepaletteshouldupdate-method"></a><span data-ttu-id="40f89-103">Método CImagePalette. ShouldUpdate</span><span class="sxs-lookup"><span data-stu-id="40f89-103">CImagePalette.ShouldUpdate method</span></span>

<span data-ttu-id="40f89-104">O `ShouldUpdate` método determina se é necessário criar uma nova paleta.</span><span class="sxs-lookup"><span data-stu-id="40f89-104">The `ShouldUpdate` method determines whether it is necessary to create a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="40f89-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40f89-105">Syntax</span></span>


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a><span data-ttu-id="40f89-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40f89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40f89-107">*pNewInfo*</span><span class="sxs-lookup"><span data-stu-id="40f89-107">*pNewInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="40f89-108">Ponteiro para uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contém a nova tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="40f89-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure containing the new color table.</span></span>

</dd> <dt>

<span data-ttu-id="40f89-109">*pOldInfo*</span><span class="sxs-lookup"><span data-stu-id="40f89-109">*pOldInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="40f89-110">Ponteiro para uma estrutura **VIDEOINFOHEADER** que contém a tabela de cores antiga.</span><span class="sxs-lookup"><span data-stu-id="40f89-110">Pointer to a **VIDEOINFOHEADER** structure containing the old color table.</span></span> <span data-ttu-id="40f89-111">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="40f89-111">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40f89-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40f89-112">Return value</span></span>

<span data-ttu-id="40f89-113">Retornará **true** se a paleta precisar ser atualizada ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="40f89-113">Returns **TRUE** if the palette needs to be updated, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="40f89-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="40f89-114">Remarks</span></span>

-   <span data-ttu-id="40f89-115">Se nenhuma estrutura **VIDEOINFOHEADER** contiver uma tabela de cores, o método retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="40f89-115">If neither **VIDEOINFOHEADER** structure contains a color table, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="40f89-116">Se apenas uma estrutura contiver uma tabela de cores ou se *pOldInfo* for **NULL**, o método retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="40f89-116">If only one structure contains a color table, or if *pOldInfo* is **NULL**, the method returns **TRUE**.</span></span>
-   <span data-ttu-id="40f89-117">Se ambas as estruturas contiverem tabelas de cores e as entradas de cor corresponderem, o método retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="40f89-117">If both structures contain color tables, and the color entries match, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="40f89-118">Se ambas as estruturas contiverem tabelas de cores, mas as entradas de cor não corresponderem, o método retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="40f89-118">If both structures contain color tables, but the color entries do not match, the method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="40f89-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40f89-119">Requirements</span></span>



| <span data-ttu-id="40f89-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="40f89-120">Requirement</span></span> | <span data-ttu-id="40f89-121">Valor</span><span class="sxs-lookup"><span data-stu-id="40f89-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40f89-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40f89-122">Header</span></span><br/>  | <dl> <span data-ttu-id="40f89-123"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40f89-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="40f89-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40f89-124">Library</span></span><br/> | <dl> <span data-ttu-id="40f89-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="40f89-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40f89-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="40f89-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f89-127">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="40f89-127">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




