---
description: Especifica se um estilo sem cor tem o estilo negrito.
ms.assetid: fd34af7f-8847-43aa-9e69-264a08eba98b
title: Função FBoldIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FBoldIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: f54e62feae710dd51cae688d380ccf7da1eda4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750164"
---
# <a name="fboldimestyle-function"></a><span data-ttu-id="a1579-103">Função FBoldIMEStyle</span><span class="sxs-lookup"><span data-stu-id="a1579-103">FBoldIMEStyle function</span></span>

<span data-ttu-id="a1579-104">Especifica se um estilo sem cor tem o estilo negrito.</span><span class="sxs-lookup"><span data-stu-id="a1579-104">Specifies whether a non-color style has the bold style.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1579-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1579-105">Syntax</span></span>


```C++
BOOL FBoldIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="a1579-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1579-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1579-107">*pimestyle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a1579-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1579-108">Uma estrutura **IMESTYLE** retornada da função [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="a1579-108">An **IMESTYLE** structure returned from the [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1579-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1579-109">Return value</span></span>

<span data-ttu-id="a1579-110">**True** se o estilo tiver o estilo negrito.</span><span class="sxs-lookup"><span data-stu-id="a1579-110">**TRUE** if the style has the bold style.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1579-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1579-111">Remarks</span></span>

<span data-ttu-id="a1579-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a1579-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1579-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1579-113">Requirements</span></span>



| <span data-ttu-id="a1579-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1579-114">Requirement</span></span> | <span data-ttu-id="a1579-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a1579-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1579-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a1579-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a1579-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1579-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1579-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1579-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1579-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="a1579-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
