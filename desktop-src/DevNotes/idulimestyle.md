---
description: Identifica se o estilo sem cor especificado tem sublinhado.
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: Função IdUlIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752574"
---
# <a name="idulimestyle-function"></a><span data-ttu-id="35006-103">Função IdUlIMEStyle</span><span class="sxs-lookup"><span data-stu-id="35006-103">IdUlIMEStyle function</span></span>

<span data-ttu-id="35006-104">Identifica se o estilo sem cor especificado tem sublinhado.</span><span class="sxs-lookup"><span data-stu-id="35006-104">Identifies whether the specified non-color style has underline.</span></span>

## <a name="syntax"></a><span data-ttu-id="35006-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35006-105">Syntax</span></span>


```C++
UINT __cdecl IdUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="35006-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35006-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35006-107">*pimestyle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35006-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35006-108">Uma estrutura **IMESTYLE** retornada da função [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="35006-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35006-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35006-109">Return value</span></span>

<span data-ttu-id="35006-110">Essa função pode retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="35006-110">This function can returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="35006-111">**IMESTY \_ UL \_ mín** (2002)</span><span class="sxs-lookup"><span data-stu-id="35006-111">**IMESTY\_UL\_MIN** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="35006-112">**IMESTY \_ UL \_ None** (2002)</span><span class="sxs-lookup"><span data-stu-id="35006-112">**IMESTY\_UL\_NONE** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="35006-113">**IMESTY \_ UL \_ único** (2003)</span><span class="sxs-lookup"><span data-stu-id="35006-113">**IMESTY\_UL\_SINGLE** (2003)</span></span>
</dt> <dt>

<span data-ttu-id="35006-114">**IMESTY \_ UL \_ pontilhado** (2005)</span><span class="sxs-lookup"><span data-stu-id="35006-114">**IMESTY\_UL\_DOTTED** (2005)</span></span>
</dt> <dt>

<span data-ttu-id="35006-115">**IMESTY \_ UL \_ espessa** (2006)</span><span class="sxs-lookup"><span data-stu-id="35006-115">**IMESTY\_UL\_THICK** (2006)</span></span>
</dt> <dt>

<span data-ttu-id="35006-116">**IMESTY \_ UL \_ inferior** (2011)</span><span class="sxs-lookup"><span data-stu-id="35006-116">**IMESTY\_UL\_LOWER** (2011)</span></span>
</dt> <dt>

<span data-ttu-id="35006-117">**IMESTY \_ UL \_ THICKLOWER** (2012)</span><span class="sxs-lookup"><span data-stu-id="35006-117">**IMESTY\_UL\_THICKLOWER** (2012)</span></span>
</dt> <dt>

<span data-ttu-id="35006-118">**IMESTY \_ UL \_ THICKDITHLOWER** (2013)</span><span class="sxs-lookup"><span data-stu-id="35006-118">**IMESTY\_UL\_THICKDITHLOWER** (2013)</span></span>
</dt> <dt>

<span data-ttu-id="35006-119">**IMESTY \_ UL \_ DITHLOWER** (2014)</span><span class="sxs-lookup"><span data-stu-id="35006-119">**IMESTY\_UL\_DITHLOWER** (2014)</span></span>
</dt> <dt>

<span data-ttu-id="35006-120">**IMESTY \_ UL \_ Max** (2014)</span><span class="sxs-lookup"><span data-stu-id="35006-120">**IMESTY\_UL\_MAX** (2014)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="35006-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="35006-121">Remarks</span></span>

<span data-ttu-id="35006-122">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="35006-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="35006-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35006-123">Requirements</span></span>



| <span data-ttu-id="35006-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="35006-124">Requirement</span></span> | <span data-ttu-id="35006-125">Valor</span><span class="sxs-lookup"><span data-stu-id="35006-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35006-126">DLL</span><span class="sxs-lookup"><span data-stu-id="35006-126">DLL</span></span><br/> | <dl> <span data-ttu-id="35006-127"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35006-127"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35006-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="35006-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35006-129">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="35006-129">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
