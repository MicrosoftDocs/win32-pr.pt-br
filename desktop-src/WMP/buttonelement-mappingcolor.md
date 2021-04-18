---
title: BUTTONelement. mappingColor
description: O atributo mappingColor especifica ou recupera a chave de cor que identifica esse BUTTONelement no botão.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- BUTTONelement. mappingColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781273"
---
# <a name="buttonelementmappingcolor"></a><span data-ttu-id="6d526-104">BUTTONelement. mappingColor</span><span class="sxs-lookup"><span data-stu-id="6d526-104">BUTTONELEMENT.mappingColor</span></span>

<span data-ttu-id="6d526-105">O atributo **mappingColor** especifica ou recupera a chave de cor que identifica esse **buttonelement** no **botão**.</span><span class="sxs-lookup"><span data-stu-id="6d526-105">The **mappingColor** attribute specifies or retrieves the color key that identifies this **BUTTONELEMENT** in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a><span data-ttu-id="6d526-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6d526-106">Possible Values</span></span>

<span data-ttu-id="6d526-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém qualquer valor de cor do Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="6d526-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="6d526-108">Não tem nenhum valor padrão.</span><span class="sxs-lookup"><span data-stu-id="6d526-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d526-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d526-109">Remarks</span></span>

<span data-ttu-id="6d526-110">Esse atributo especifica a cor da região no grupo de botões **mappingImage** que corresponde a esse elemento Button.</span><span class="sxs-lookup"><span data-stu-id="6d526-110">This attribute specifies the color of the region in the button group **mappingImage** that corresponds to this button element.</span></span> <span data-ttu-id="6d526-111">Todos os cliques nessa região são tratados por este elemento Button.</span><span class="sxs-lookup"><span data-stu-id="6d526-111">All clicks on this region are handled by this button element.</span></span>

<span data-ttu-id="6d526-112">Se uma cor inválida for especificada, o **botãoelement** não será ativado.</span><span class="sxs-lookup"><span data-stu-id="6d526-112">If an invalid color is specified, the **BUTTONELEMENT** is not activated.</span></span>

## <a name="examples"></a><span data-ttu-id="6d526-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d526-113">Examples</span></span>

<span data-ttu-id="6d526-114">O exemplo a seguir é um arquivo de definição de capa completa que ilustra como alguns dos atributos **buttonelement** são usados.</span><span class="sxs-lookup"><span data-stu-id="6d526-114">The following sample is a complete skin definition file that illustrates how some of the **BUTTONELEMENT** attributes are used.</span></span> <span data-ttu-id="6d526-115">Ele pode ser encontrado no diretório de exemplos que foi instalado com o SDK.</span><span class="sxs-lookup"><span data-stu-id="6d526-115">It can be found in the Samples directory that was installed with the SDK.</span></span>


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
    />
    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    >
      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />
      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />
    </BUTTONGROUP>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="6d526-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d526-116">Requirements</span></span>



| <span data-ttu-id="6d526-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d526-117">Requirement</span></span> | <span data-ttu-id="6d526-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6d526-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6d526-119">Versão</span><span class="sxs-lookup"><span data-stu-id="6d526-119">Version</span></span><br/> | <span data-ttu-id="6d526-120">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6d526-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d526-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d526-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d526-122">**Referência de cor**</span><span class="sxs-lookup"><span data-stu-id="6d526-122">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="6d526-123">**Elemento BUTTONelement**</span><span class="sxs-lookup"><span data-stu-id="6d526-123">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="6d526-124">**BUTTON. mappingImage**</span><span class="sxs-lookup"><span data-stu-id="6d526-124">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





