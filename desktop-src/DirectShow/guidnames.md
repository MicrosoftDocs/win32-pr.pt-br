---
description: GuidNames é uma matriz global na biblioteca de classes base do DirectShow que contém cadeias de caracteres que representam os GUIDs definidos em UUIDs. h. Essa matriz é útil para gerar a saída de depuração.
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: GuidNames (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778479"
---
# <a name="guidnames"></a><span data-ttu-id="440b1-104">GuidNames</span><span class="sxs-lookup"><span data-stu-id="440b1-104">GuidNames</span></span>

<span data-ttu-id="440b1-105">`GuidNames` é uma matriz global na biblioteca de classes base do DirectShow que contém cadeias de caracteres que representam os GUIDs definidos em UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="440b1-105">`GuidNames` is a global array in the DirectShow base class library that contains strings representing the GUIDs defined in Uuids.h.</span></span> <span data-ttu-id="440b1-106">Essa matriz é útil para gerar a saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="440b1-106">This array is useful for generating debug output.</span></span>

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a><span data-ttu-id="440b1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="440b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="440b1-108"><span id="guid"></span><span id="GUID"></span>*volume*</span><span class="sxs-lookup"><span data-stu-id="440b1-108"><span id="guid"></span><span id="GUID"></span>*guid*</span></span>
</dt> <dd>

<span data-ttu-id="440b1-109">Especifica qualquer valor de GUID definido no arquivo de cabeçalho UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="440b1-109">Specifies any GUID value defined in the header file Uuids.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="440b1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="440b1-110">Remarks</span></span>

<span data-ttu-id="440b1-111">Use essa matriz global para gerar constantes de GUID como cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="440b1-111">Use this global array to output GUID constants as strings.</span></span> <span data-ttu-id="440b1-112">Por exemplo, o código a seguir imprime a cadeia de caracteres " \_ vídeo de MediaType" no console:</span><span class="sxs-lookup"><span data-stu-id="440b1-112">For example, the following code prints the string "MEDIATYPE\_Video" to the console:</span></span>


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



<span data-ttu-id="440b1-113">Se o GUID não for correspondido, a cadeia de caracteres "nome de GUID desconhecido" será retornada.</span><span class="sxs-lookup"><span data-stu-id="440b1-113">If the GUID is not matched, the string "Unknown GUID Name" is returned.</span></span> <span data-ttu-id="440b1-114">Nem todos os GUIDs do DirectShow são definidos em UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="440b1-114">Not all DirectShow GUIDs are defined in uuids.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="440b1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="440b1-115">Requirements</span></span>



| <span data-ttu-id="440b1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="440b1-116">Requirement</span></span> | <span data-ttu-id="440b1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="440b1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="440b1-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="440b1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="440b1-119"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="440b1-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="440b1-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="440b1-120">Library</span></span><br/> | <dl> <span data-ttu-id="440b1-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="440b1-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="440b1-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="440b1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="440b1-123">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="440b1-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




