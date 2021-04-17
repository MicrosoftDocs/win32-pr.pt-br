---
title: ClosedCaption. SAMIstyle
description: A propriedade SAMIstyle especifica ou recupera o estilo de legenda oculta.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- ClosedCaption. SAMIstyle Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe81c2c2c4f4504d6167abe538c52ab769550a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762093"
---
# <a name="closedcaptionsamistyle"></a><span data-ttu-id="6106e-104">ClosedCaption. SAMIstyle</span><span class="sxs-lookup"><span data-stu-id="6106e-104">ClosedCaption.SAMIStyle</span></span>

<span data-ttu-id="6106e-105">A propriedade **samistyle** especifica ou recupera o estilo de legenda oculta.</span><span class="sxs-lookup"><span data-stu-id="6106e-105">The **SAMIStyle** property specifies or retrieves the closed captioning style.</span></span>

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a><span data-ttu-id="6106e-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6106e-106">Possible Values</span></span>

<span data-ttu-id="6106e-107">Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6106e-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6106e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6106e-108">Remarks</span></span>

<span data-ttu-id="6106e-109">Um arquivo SAMI pode conter várias definições de estilo de formato.</span><span class="sxs-lookup"><span data-stu-id="6106e-109">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="6106e-110">Os estilos SAMI são definidos entre as marcas <STYLE> e </STYLE> no arquivo Sami.</span><span class="sxs-lookup"><span data-stu-id="6106e-110">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="6106e-111">Um estilo é definido com uma cadeia de caracteres de texto precedida por um \# caractere.</span><span class="sxs-lookup"><span data-stu-id="6106e-111">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="6106e-112">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6106e-112">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



<span data-ttu-id="6106e-113">Isso especifica um estilo que produz uma fonte específica.</span><span class="sxs-lookup"><span data-stu-id="6106e-113">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="6106e-114">Se nenhum estilo SAMI for especificado, o primeiro estilo definido no arquivo SAMI será usado por padrão.</span><span class="sxs-lookup"><span data-stu-id="6106e-114">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="6106e-115">**Windows Media Player 10 Mobile:** Essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="6106e-115">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="6106e-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6106e-116">Examples</span></span>

<span data-ttu-id="6106e-117">O exemplo de JScript a seguir cria um elemento HTML SELECT que usa *closedCaption*. **Samistyle** para alterar a aparência do texto da legenda oculta.</span><span class="sxs-lookup"><span data-stu-id="6106e-117">The following JScript example creates an HTML SELECT element that uses *closedCaption*.**SAMIStyle** to change the appearance of the closed caption text.</span></span> <span data-ttu-id="6106e-118">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6106e-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="6106e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6106e-119">Requirements</span></span>



| <span data-ttu-id="6106e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6106e-120">Requirement</span></span> | <span data-ttu-id="6106e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6106e-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6106e-122">Versão</span><span class="sxs-lookup"><span data-stu-id="6106e-122">Version</span></span><br/> | <span data-ttu-id="6106e-123">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6106e-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6106e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6106e-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="6106e-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6106e-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6106e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6106e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6106e-127">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="6106e-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="6106e-128">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="6106e-128">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





