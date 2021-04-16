---
description: O método SetFormat Inicializa o bloco de formato.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Método CMediaType. SetFormat (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08dd05faf514581a3325f4922076ba2053cd0c95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775629"
---
# <a name="cmediatypesetformat-method"></a><span data-ttu-id="b43ca-103">Método CMediaType. SetFormat</span><span class="sxs-lookup"><span data-stu-id="b43ca-103">CMediaType.SetFormat method</span></span>

<span data-ttu-id="b43ca-104">O `SetFormat` método inicializa o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="b43ca-104">The `SetFormat` method initializes the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="b43ca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b43ca-105">Syntax</span></span>


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="b43ca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b43ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b43ca-107">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="b43ca-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="b43ca-108">Ponteiro para um bloco de memória que contém o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="b43ca-108">Pointer to a block of memory that contains the format block.</span></span>

</dd> <dt>

<span data-ttu-id="b43ca-109">*length*</span><span class="sxs-lookup"><span data-stu-id="b43ca-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="b43ca-110">Comprimento do bloco de formato, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b43ca-110">Length of the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b43ca-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b43ca-111">Return value</span></span>

<span data-ttu-id="b43ca-112">Retornará **true** se for bem-sucedido ou **false** se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="b43ca-112">Returns **TRUE** if successful, or **FALSE** if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="b43ca-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b43ca-113">Remarks</span></span>

<span data-ttu-id="b43ca-114">Esse método aloca memória para o bloco de formato e copia o buffer especificado por *pFormat* no novo bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="b43ca-114">This method allocates memory for the format block and copies the buffer specified by *pFormat* into the new format block.</span></span> <span data-ttu-id="b43ca-115">Se o tipo de mídia já contiver um bloco de formato, o antigo será liberado.</span><span class="sxs-lookup"><span data-stu-id="b43ca-115">If the media type already contains a format block, the old one is released.</span></span> <span data-ttu-id="b43ca-116">O método também define o membro **cbFormat** da estrutura **do \_ \_ tipo de mídia am** .</span><span class="sxs-lookup"><span data-stu-id="b43ca-116">The method also sets the **cbFormat** member of the **AM\_MEDIA\_TYPE** structure.</span></span>

<span data-ttu-id="b43ca-117">Para definir o tipo de formato, chame o método [**CMediaType:: Setformattype**](cmediatype-setformattype.md) .</span><span class="sxs-lookup"><span data-stu-id="b43ca-117">To set the format type, call the [**CMediaType::SetFormatType**](cmediatype-setformattype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b43ca-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b43ca-118">Requirements</span></span>



| <span data-ttu-id="b43ca-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b43ca-119">Requirement</span></span> | <span data-ttu-id="b43ca-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b43ca-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b43ca-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b43ca-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b43ca-122"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b43ca-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="b43ca-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b43ca-123">Library</span></span><br/> | <dl> <span data-ttu-id="b43ca-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b43ca-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b43ca-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b43ca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b43ca-126">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="b43ca-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




