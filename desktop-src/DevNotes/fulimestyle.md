---
description: Especifica se um estilo sem cor tem um estilo sublinhado.
ms.assetid: 452dda6e-b12b-457c-9a01-c5363359c9f5
title: Função FUlIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: a49090d2ca192dfd3ec6d0064b92bd2233af79c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747881"
---
# <a name="fulimestyle-function"></a><span data-ttu-id="27d0f-103">Função FUlIMEStyle</span><span class="sxs-lookup"><span data-stu-id="27d0f-103">FUlIMEStyle function</span></span>

<span data-ttu-id="27d0f-104">Especifica se um estilo sem cor tem um estilo sublinhado.</span><span class="sxs-lookup"><span data-stu-id="27d0f-104">Specifies whether a non-color style has an underline style.</span></span>

## <a name="syntax"></a><span data-ttu-id="27d0f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27d0f-105">Syntax</span></span>


```C++
BOOL __cdecl FUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="27d0f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27d0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27d0f-107">*pimestyle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27d0f-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27d0f-108">Uma estrutura **IMESTYLE** retornada da função [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="27d0f-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27d0f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27d0f-109">Return value</span></span>

<span data-ttu-id="27d0f-110">TRUE se o estilo tiver um estilo sublinhado.</span><span class="sxs-lookup"><span data-stu-id="27d0f-110">TRUE if the style has an underline style.</span></span>

## <a name="remarks"></a><span data-ttu-id="27d0f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="27d0f-111">Remarks</span></span>

<span data-ttu-id="27d0f-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="27d0f-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="27d0f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27d0f-113">Requirements</span></span>



| <span data-ttu-id="27d0f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="27d0f-114">Requirement</span></span> | <span data-ttu-id="27d0f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="27d0f-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27d0f-116">DLL</span><span class="sxs-lookup"><span data-stu-id="27d0f-116">DLL</span></span><br/> | <dl> <span data-ttu-id="27d0f-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27d0f-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27d0f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="27d0f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27d0f-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="27d0f-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
