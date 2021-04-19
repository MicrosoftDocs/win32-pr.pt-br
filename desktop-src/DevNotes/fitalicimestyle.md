---
description: Especifica se um estilo sem cor tem o estilo itálico.
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: Função FItalicIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 828e701773d666830473e92afc73f80ccdae3bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748516"
---
# <a name="fitalicimestyle-function"></a><span data-ttu-id="4736d-103">Função FItalicIMEStyle</span><span class="sxs-lookup"><span data-stu-id="4736d-103">FItalicIMEStyle function</span></span>

<span data-ttu-id="4736d-104">Especifica se um estilo sem cor tem o estilo itálico.</span><span class="sxs-lookup"><span data-stu-id="4736d-104">Specifies whether a non-color style has the italic style.</span></span>

## <a name="syntax"></a><span data-ttu-id="4736d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4736d-105">Syntax</span></span>


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="4736d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4736d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4736d-107">*pimestyle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4736d-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4736d-108">Uma estrutura **IMESTYLE** retornada da função [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="4736d-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4736d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4736d-109">Return value</span></span>

<span data-ttu-id="4736d-110">**True** se o estilo tiver o estilo itálico.</span><span class="sxs-lookup"><span data-stu-id="4736d-110">**TRUE** if the style has the italic style.</span></span>

## <a name="remarks"></a><span data-ttu-id="4736d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4736d-111">Remarks</span></span>

<span data-ttu-id="4736d-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4736d-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4736d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4736d-113">Requirements</span></span>



| <span data-ttu-id="4736d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4736d-114">Requirement</span></span> | <span data-ttu-id="4736d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4736d-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4736d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="4736d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="4736d-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4736d-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4736d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="4736d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4736d-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="4736d-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
