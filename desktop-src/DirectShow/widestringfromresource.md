---
description: A função WideStringFromResource carrega uma cadeia de caracteres largos de um arquivo de recurso com o identificador de recurso fornecido.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: Função WideStringFromResource (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c7cbdccc76fc57e660109851ae5b8f141704d04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756781"
---
# <a name="widestringfromresource-function"></a><span data-ttu-id="1a5c1-103">Função WideStringFromResource</span><span class="sxs-lookup"><span data-stu-id="1a5c1-103">WideStringFromResource function</span></span>

<span data-ttu-id="1a5c1-104">A `WideStringFromResource` função carrega uma cadeia de caracteres largos de um arquivo de recurso com o identificador de recurso fornecido.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-104">The `WideStringFromResource` function loads a wide-character string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a5c1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a5c1-105">Syntax</span></span>


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="1a5c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a5c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a5c1-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="1a5c1-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="1a5c1-108">Ponteiro para a cadeia de caracteres correspondente a *iResourceID*.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="1a5c1-109">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="1a5c1-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="1a5c1-110">Identificador de recurso da cadeia de caracteres a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a5c1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a5c1-111">Return value</span></span>

<span data-ttu-id="1a5c1-112">Retorna a mesma cadeia de caracteres de *pBuffer*.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="1a5c1-113">Se a função não for bem-sucedida, retorna uma cadeia de caracteres nula.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a5c1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a5c1-114">Remarks</span></span>

<span data-ttu-id="1a5c1-115">As páginas de propriedades são geralmente chamadas por meio de suas interfaces COM, que usam cadeias de caracteres largos, independentemente de como o binário é compilado.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-115">Property pages are typically called through their COM interfaces, which use wide-character strings regardless of how the binary is built.</span></span> <span data-ttu-id="1a5c1-116">Essa função permite converter uma cadeia de caracteres de recurso em uma cadeia de caracteres largos.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-116">This function allows you to convert a resource string to a wide-character string.</span></span> <span data-ttu-id="1a5c1-117">A função converte o recurso em uma cadeia de caracteres largos (se ainda não for um) depois de carregá-lo.</span><span class="sxs-lookup"><span data-stu-id="1a5c1-117">The function converts the resource to a wide-character string (if it is not already one) after loading it.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a5c1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a5c1-118">Requirements</span></span>



| <span data-ttu-id="1a5c1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a5c1-119">Requirement</span></span> | <span data-ttu-id="1a5c1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1a5c1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a5c1-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a5c1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1a5c1-122"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a5c1-122"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1a5c1-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a5c1-123">Library</span></span><br/> | <dl> <span data-ttu-id="1a5c1-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1a5c1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a5c1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a5c1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a5c1-126">Funções auxiliares de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="1a5c1-126">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




