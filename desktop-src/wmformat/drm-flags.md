---
title: DRM_Flags
description: A \_ propriedade de sinalizadores DRM é usada com o conteúdo do DRM versão 1 somente para especificar os direitos que estarão contidos na licença local.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags o formato Windows Media
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916987"
---
# <a name="drm_flags"></a><span data-ttu-id="4077d-104">Sinalizadores de DRM \_</span><span class="sxs-lookup"><span data-stu-id="4077d-104">DRM\_Flags</span></span>

<span data-ttu-id="4077d-105">A propriedade de **\_ sinalizadores DRM** é usada com o conteúdo do DRM versão 1 somente para especificar os direitos que estarão contidos na licença local.</span><span class="sxs-lookup"><span data-stu-id="4077d-105">The **DRM\_Flags** property is used with DRM version 1 content only to specify the rights that will be contained in the local license.</span></span> <span data-ttu-id="4077d-106">Os direitos são especificados com valores definidos pelo tipo de enumeração **\_ direitos de WMT** .</span><span class="sxs-lookup"><span data-stu-id="4077d-106">Rights are specified with values defined by the **WMT\_RIGHTS** enumeration type.</span></span> <span data-ttu-id="4077d-107">Mais de um valor pode ser selecionado combinando-os com o **operador OR**</span><span class="sxs-lookup"><span data-stu-id="4077d-107">More than one value can be selected by combining them with the bitwise **OR** operator.</span></span>

## <a name="global-constant"></a><span data-ttu-id="4077d-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="4077d-108">Global Constant</span></span>

<span data-ttu-id="4077d-109">\_sinalizadores g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="4077d-109">g\_wszWMDRM\_Flags</span></span>

## <a name="data-type"></a><span data-ttu-id="4077d-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="4077d-110">Data Type</span></span>

<span data-ttu-id="4077d-111">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4077d-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="4077d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4077d-112">Remarks</span></span>

<span data-ttu-id="4077d-113">Ao acessar a interface **IWMHeaderInfo3** do objeto gravador, você pode adicionar ou alterar esse valor.</span><span class="sxs-lookup"><span data-stu-id="4077d-113">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="4077d-114">Em outros objetos (editor de metadados, leitor e leitor síncrono), esse valor é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4077d-114">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span> <span data-ttu-id="4077d-115">Use [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) para definir essa propriedade ao criar o conteúdo do DRM versão 1.</span><span class="sxs-lookup"><span data-stu-id="4077d-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when creating DRM version 1 content.</span></span>

## <a name="see-also"></a><span data-ttu-id="4077d-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="4077d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4077d-117">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="4077d-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




