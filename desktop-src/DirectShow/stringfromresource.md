---
description: A função StringFromResource carrega uma cadeia de caracteres de um arquivo de recurso com o identificador de recurso fornecido.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Função StringFromResource (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758669"
---
# <a name="stringfromresource-function"></a><span data-ttu-id="62793-103">Função StringFromResource</span><span class="sxs-lookup"><span data-stu-id="62793-103">StringFromResource function</span></span>

<span data-ttu-id="62793-104">A `StringFromResource` função carrega uma cadeia de caracteres de um arquivo de recurso com o identificador de recurso fornecido.</span><span class="sxs-lookup"><span data-stu-id="62793-104">The `StringFromResource` function loads a string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="62793-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62793-105">Syntax</span></span>


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="62793-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62793-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62793-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="62793-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="62793-108">Ponteiro para a cadeia de caracteres correspondente a *iResourceID*.</span><span class="sxs-lookup"><span data-stu-id="62793-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="62793-109">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="62793-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="62793-110">Identificador de recurso da cadeia de caracteres a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="62793-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62793-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62793-111">Return value</span></span>

<span data-ttu-id="62793-112">Retorna a mesma cadeia de caracteres de *pBuffer*.</span><span class="sxs-lookup"><span data-stu-id="62793-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="62793-113">Se a função não for bem-sucedida, retorna uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="62793-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="62793-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="62793-114">Remarks</span></span>

<span data-ttu-id="62793-115">O buffer *pBuffer* deve ter no mínimo \_ bytes de comprimento máximo de Str \_ .</span><span class="sxs-lookup"><span data-stu-id="62793-115">The *pBuffer* buffer must be at least STR\_MAX\_LENGTH bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="62793-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62793-116">Requirements</span></span>



| <span data-ttu-id="62793-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="62793-117">Requirement</span></span> | <span data-ttu-id="62793-118">Valor</span><span class="sxs-lookup"><span data-stu-id="62793-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62793-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62793-119">Header</span></span><br/>  | <dl> <span data-ttu-id="62793-120"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62793-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="62793-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62793-121">Library</span></span><br/> | <dl> <span data-ttu-id="62793-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="62793-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62793-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="62793-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62793-124">Funções auxiliares de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="62793-124">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




