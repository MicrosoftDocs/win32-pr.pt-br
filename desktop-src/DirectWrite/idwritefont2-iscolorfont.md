---
title: Método IDWriteFont2 IsColorFont
description: Permite determinar se um caminho de renderização de cor é potencialmente necessário.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Gravação direta do método IsColorFont
- Método IsColorFont Direct Write, interface IDWriteFont2
- IDWriteFont2 interface de gravação direta, método IsColorFont
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369748"
---
# <a name="idwritefont2iscolorfont-method"></a><span data-ttu-id="f0095-106">Método IDWriteFont2:: IsColorFont</span><span class="sxs-lookup"><span data-stu-id="f0095-106">IDWriteFont2::IsColorFont method</span></span>

<span data-ttu-id="f0095-107">Permite determinar se um caminho de renderização de cor é potencialmente necessário.</span><span class="sxs-lookup"><span data-stu-id="f0095-107">Enables determining if a color rendering path is potentially necessary.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0095-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0095-108">Syntax</span></span>


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a><span data-ttu-id="f0095-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0095-109">Parameters</span></span>

<span data-ttu-id="f0095-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f0095-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0095-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0095-111">Return value</span></span>

<span data-ttu-id="f0095-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="f0095-112">Type: **BOOL**</span></span>

<span data-ttu-id="f0095-113">Retornará **true** se a fonte tiver informações de cor (tabelas COLR e Cpal); caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="f0095-113">Returns **TRUE** if the font has color information (COLR and CPAL tables); otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0095-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0095-114">Requirements</span></span>



| <span data-ttu-id="f0095-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0095-115">Requirement</span></span> | <span data-ttu-id="f0095-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f0095-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0095-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0095-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f0095-118">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f0095-118">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="f0095-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0095-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f0095-120">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f0095-120">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="f0095-121">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="f0095-121">Minimum supported phone</span></span><br/>  | <span data-ttu-id="f0095-122">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="f0095-122">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="f0095-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0095-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0095-124"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0095-124"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f0095-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f0095-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0095-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0095-126"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f0095-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0095-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0095-128">**IDWriteFont2**</span><span class="sxs-lookup"><span data-stu-id="f0095-128">**IDWriteFont2**</span></span>](idwritefont2.md)
</dt> </dl>

 

 





