---
description: A função ValidateBitmapInfoHeader verifica uma estrutura de BITMAPINFOHEADER para determinados erros comuns que podem causar estouros de buffer ou estouro de número inteiro.
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: Função ValidateBitmapInfoHeader (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759108"
---
# <a name="validatebitmapinfoheader-function"></a><span data-ttu-id="06bc3-103">Função ValidateBitmapInfoHeader</span><span class="sxs-lookup"><span data-stu-id="06bc3-103">ValidateBitmapInfoHeader function</span></span>

<span data-ttu-id="06bc3-104">A `ValidateBitmapInfoHeader` função verifica uma estrutura de [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) para determinados erros comuns que podem causar estouros de buffer ou estouro de número inteiro.</span><span class="sxs-lookup"><span data-stu-id="06bc3-104">The `ValidateBitmapInfoHeader` function checks a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="06bc3-105">Essa função não garante que a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seja válida ou que o código que usa a estrutura seja seguro.</span><span class="sxs-lookup"><span data-stu-id="06bc3-105">This function does not guarantee that the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="06bc3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06bc3-106">Syntax</span></span>


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="06bc3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06bc3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06bc3-108">*pbmi*</span><span class="sxs-lookup"><span data-stu-id="06bc3-108">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="06bc3-109">Ponteiro para a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) a ser validada.</span><span class="sxs-lookup"><span data-stu-id="06bc3-109">Pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure to validate.</span></span>

</dd> <dt>

<span data-ttu-id="06bc3-110">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="06bc3-110">*cbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="06bc3-111">Tamanho do bloco de memória que contém a estrutura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="06bc3-111">Size of the memory block that holds the structure, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06bc3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06bc3-112">Return value</span></span>

<span data-ttu-id="06bc3-113">Retorna um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="06bc3-113">Returns a Boolean value.</span></span> <span data-ttu-id="06bc3-114">Se o valor for **false**, a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) não será válida.</span><span class="sxs-lookup"><span data-stu-id="06bc3-114">If the value is **FALSE**, the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="06bc3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="06bc3-115">Remarks</span></span>

<span data-ttu-id="06bc3-116">Essa função protege os seguintes erros:</span><span class="sxs-lookup"><span data-stu-id="06bc3-116">This function guards against the following errors:</span></span>

-   <span data-ttu-id="06bc3-117">Estouro aritmético no tamanho da estrutura ou em um tamanho de estrutura inválido.</span><span class="sxs-lookup"><span data-stu-id="06bc3-117">Arithmetic overflow in the structure size or an invalid structure size.</span></span>
-   <span data-ttu-id="06bc3-118">Valor inválido para o membro **biClrUsed** .</span><span class="sxs-lookup"><span data-stu-id="06bc3-118">Invalid value for the **biClrUsed** member.</span></span>
-   <span data-ttu-id="06bc3-119">Estouro aritmético no tamanho da imagem (**biSizeImage**).</span><span class="sxs-lookup"><span data-stu-id="06bc3-119">Arithmetic overflow in the image size (**biSizeImage**).</span></span>
-   <span data-ttu-id="06bc3-120">Valores inválidos para o tamanho da imagem (**biSizeImage**) para formatos RGB.</span><span class="sxs-lookup"><span data-stu-id="06bc3-120">Invalid values for the image size (**biSizeImage**) for RGB formats.</span></span>

<span data-ttu-id="06bc3-121">A função não verifica se a estrutura descreve um formato de vídeo válido.</span><span class="sxs-lookup"><span data-stu-id="06bc3-121">The function does not check whether the structure describes a valid video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="06bc3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06bc3-122">Requirements</span></span>



| <span data-ttu-id="06bc3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="06bc3-123">Requirement</span></span> | <span data-ttu-id="06bc3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="06bc3-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06bc3-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06bc3-125">Header</span></span><br/> | <dl> <span data-ttu-id="06bc3-126"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="06bc3-126"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06bc3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="06bc3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06bc3-128">Funções de vídeo e imagem</span><span class="sxs-lookup"><span data-stu-id="06bc3-128">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




