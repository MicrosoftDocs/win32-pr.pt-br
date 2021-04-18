---
title: UI_PKEY_FontProperties_Family
description: Identifica a \_ \_ propriedade da família PKEY fontproperties da interface do usuário \_ .
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7183e51105a397f14154639512ca11f7c03d44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789400"
---
# <a name="ui_pkey_fontproperties_family"></a><span data-ttu-id="62c0e-103">IU \_ \_ da família PKEY fontproperties \_</span><span class="sxs-lookup"><span data-stu-id="62c0e-103">UI\_PKEY\_FontProperties\_Family</span></span>

<span data-ttu-id="62c0e-104">Identifica a \_ \_ propriedade da família PKEY fontproperties da interface do usuário \_ .</span><span class="sxs-lookup"><span data-stu-id="62c0e-104">Identifies the UI\_PKEY\_FontProperties\_Family property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="62c0e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="62c0e-105">Remarks</span></span>

<span data-ttu-id="62c0e-106">Interface do usuário \_ PKEY \_ fontproperties \_ Family é usada por um aplicativo para consultar o valor da Galeria suspensa **família de fontes** .</span><span class="sxs-lookup"><span data-stu-id="62c0e-106">UI\_PKEY\_FontProperties\_Family is used by an application to query the value of the **Font family** drop-down gallery.</span></span>

<span data-ttu-id="62c0e-107">O valor da família da interface do usuário \_ PKEY \_ fontproperties \_ corresponde a um nome de [famílias de fontes GDI do Windows](../gdi/font-families.md) recuperado com a [função EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) ou a [função EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).</span><span class="sxs-lookup"><span data-stu-id="62c0e-107">The value of UI\_PKEY\_FontProperties\_Family matches a [Windows GDI Font Families](../gdi/font-families.md) name retrieved with the [EnumFontFamilies function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) or [EnumFontFamiliesEx function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).</span></span>

<span data-ttu-id="62c0e-108">O valor padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="62c0e-108">The default value is an empty string.</span></span>

<span data-ttu-id="62c0e-109">Se uma cadeia de caracteres vazia for fornecida para o valor para a família de fontes PKEY da interface do usuário \_ \_ \_ , a seleção de fonte será desmarcada.</span><span class="sxs-lookup"><span data-stu-id="62c0e-109">If an empty string is supplied for the value for UI\_PKEY\_FontProperties\_Family, then the font selection is cleared.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62c0e-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62c0e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62c0e-111">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="62c0e-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="62c0e-112">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="62c0e-112">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 