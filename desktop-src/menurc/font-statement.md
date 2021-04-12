---
title: Instrução FONT
description: Define a fonte com a qual o sistema irá desenhar texto na caixa de diálogo. A fonte deve ter sido carregada anteriormente; por exemplo, chamando a função LoadResource.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Menus de instrução de fonte e outros recursos
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b31b280a5a973301e8410f1f74340138af07ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454048"
---
# <a name="font-statement"></a><span data-ttu-id="eda81-105">Instrução FONT</span><span class="sxs-lookup"><span data-stu-id="eda81-105">FONT statement</span></span>

<span data-ttu-id="eda81-106">Define a fonte com a qual o sistema irá desenhar texto na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="eda81-106">Defines the font with which the system will draw text in the dialog box.</span></span> <span data-ttu-id="eda81-107">A fonte deve ter sido carregada anteriormente; por exemplo, chamando a função [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .</span><span class="sxs-lookup"><span data-stu-id="eda81-107">The font must have been previously loaded; for example, by calling the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span data-ttu-id="eda81-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*pontos*</span><span class="sxs-lookup"><span data-stu-id="eda81-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*</span></span>
</dt> <dd>

<span data-ttu-id="eda81-109">O tamanho da fonte, em pontos.</span><span class="sxs-lookup"><span data-stu-id="eda81-109">The size of the font, in points.</span></span>

</dd> <dt>

<span data-ttu-id="eda81-110"><span id="typeface"></span><span id="TYPEFACE"></span>*face*</span><span class="sxs-lookup"><span data-stu-id="eda81-110"><span id="typeface"></span><span id="TYPEFACE"></span>*typeface*</span></span>
</dt> <dd>

<span data-ttu-id="eda81-111">O nome do tipo de fonte.</span><span class="sxs-lookup"><span data-stu-id="eda81-111">The name of the typeface.</span></span> <span data-ttu-id="eda81-112">Esse parâmetro deve ser colocado entre aspas (").</span><span class="sxs-lookup"><span data-stu-id="eda81-112">This parameter must be enclosed in quotes (").</span></span>

</dd> <dt>

<span data-ttu-id="eda81-113"><span id="weight"></span><span id="WEIGHT"></span>*largura*</span><span class="sxs-lookup"><span data-stu-id="eda81-113"><span id="weight"></span><span id="WEIGHT"></span>*weight*</span></span>
</dt> <dd>

<span data-ttu-id="eda81-114">O peso da fonte no intervalo de 0 a 1000.</span><span class="sxs-lookup"><span data-stu-id="eda81-114">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="eda81-115">Por exemplo, 400 é normal e 700 é negrito.</span><span class="sxs-lookup"><span data-stu-id="eda81-115">For example, 400 is normal and 700 is bold.</span></span> <span data-ttu-id="eda81-116">Se esse valor for 0, o peso padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="eda81-116">If this value is 0, the default weight is used.</span></span> <span data-ttu-id="eda81-117">Para obter uma lista de valores predefinidos, consulte os valores de **FW \_ \*** definidos em WinGDI. h.</span><span class="sxs-lookup"><span data-stu-id="eda81-117">For a list of predefined values, see the **FW\_\*** values defined in WinGDI.h.</span></span>

</dd> <dt>

<span data-ttu-id="eda81-118"><span id="italic"></span><span id="ITALIC"></span>*colocadas*</span><span class="sxs-lookup"><span data-stu-id="eda81-118"><span id="italic"></span><span id="ITALIC"></span>*italic*</span></span>
</dt> <dd>

<span data-ttu-id="eda81-119">Indica uma fonte em itálico se definido como TRUE.</span><span class="sxs-lookup"><span data-stu-id="eda81-119">Indicates an italic font if set to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="eda81-120"><span id="charset"></span><span id="CHARSET"></span>*charset*</span><span class="sxs-lookup"><span data-stu-id="eda81-120"><span id="charset"></span><span id="CHARSET"></span>*charset*</span></span>
</dt> <dd>

<span data-ttu-id="eda81-121">O conjunto de caracteres.</span><span class="sxs-lookup"><span data-stu-id="eda81-121">The character set.</span></span> <span data-ttu-id="eda81-122">Para obter uma lista de valores, consulte o membro **lfCharSet** da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="eda81-122">For a list of values, see the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="eda81-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eda81-123">Examples</span></span>

<span data-ttu-id="eda81-124">O exemplo a seguir demonstra o uso da instrução **Font** :</span><span class="sxs-lookup"><span data-stu-id="eda81-124">The following example demonstrates the use of the **FONT** statement:</span></span>

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a><span data-ttu-id="eda81-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="eda81-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eda81-126">**LoadResource**</span><span class="sxs-lookup"><span data-stu-id="eda81-126">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 