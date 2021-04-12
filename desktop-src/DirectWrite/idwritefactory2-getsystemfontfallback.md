---
title: Método IDWriteFactory2 GetSystemFontFallback
description: Cria um objeto de fallback de fonte da lista de fallback de fontes do sistema.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Gravação direta do método GetSystemFontFallback
- Método GetSystemFontFallback Direct Write, interface IDWriteFactory2
- IDWriteFactory2 interface de gravação direta, método GetSystemFontFallback
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f0eb73ee80dc3e6195267d25f6043225b8613ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366461"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a><span data-ttu-id="0820b-106">Método IDWriteFactory2:: GetSystemFontFallback</span><span class="sxs-lookup"><span data-stu-id="0820b-106">IDWriteFactory2::GetSystemFontFallback method</span></span>

<span data-ttu-id="0820b-107">Cria um objeto de fallback de fonte da lista de fallback de fontes do sistema.</span><span class="sxs-lookup"><span data-stu-id="0820b-107">Creates a font fallback object from the system font fallback list.</span></span>

## <a name="syntax"></a><span data-ttu-id="0820b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0820b-108">Syntax</span></span>


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a><span data-ttu-id="0820b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0820b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0820b-110">*fontFallback* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0820b-110">*fontFallback* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0820b-111">Tipo: **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***</span><span class="sxs-lookup"><span data-stu-id="0820b-111">Type: **[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***</span></span>

<span data-ttu-id="0820b-112">Contém um endereço de um ponteiro para o objeto de fallback de fonte recém-criado.</span><span class="sxs-lookup"><span data-stu-id="0820b-112">Contains an address of a pointer to the newly created font fallback object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0820b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0820b-113">Return value</span></span>

<span data-ttu-id="0820b-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0820b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0820b-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0820b-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0820b-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0820b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="0820b-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="0820b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0820b-118">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="0820b-118">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

 