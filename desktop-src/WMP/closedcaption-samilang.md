---
title: ClosedCaption.SAMILang
description: A propriedade SAMILang especifica ou recupera o idioma exibido para legendas ocultas.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- ClosedCaption. SAMILang Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781267"
---
# <a name="closedcaptionsamilang"></a><span data-ttu-id="7b4df-104">ClosedCaption.SAMILang</span><span class="sxs-lookup"><span data-stu-id="7b4df-104">ClosedCaption.SAMILang</span></span>

<span data-ttu-id="7b4df-105">A propriedade **SAMILang** especifica ou recupera o idioma exibido para legendas ocultas.</span><span class="sxs-lookup"><span data-stu-id="7b4df-105">The **SAMILang** property specifies or retrieves the language displayed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a><span data-ttu-id="7b4df-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="7b4df-106">Possible Values</span></span>

<span data-ttu-id="7b4df-107">Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7b4df-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b4df-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b4df-108">Remarks</span></span>

<span data-ttu-id="7b4df-109">Um arquivo SAMI pode conter texto para uma ou várias linguagens.</span><span class="sxs-lookup"><span data-stu-id="7b4df-109">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="7b4df-110">Os idiomas disponíveis para legendas codificadas são definidos entre as marcas <STYLE> e </STYLE> no arquivo Sami.</span><span class="sxs-lookup"><span data-stu-id="7b4df-110">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="7b4df-111">Um identificador de idioma é especificado com uma cadeia de caracteres alfanumérica exclusiva que é precedida por um ponto (.).</span><span class="sxs-lookup"><span data-stu-id="7b4df-111">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="7b4df-112">O nome especificado para um idioma pode ser qualquer cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7b4df-112">The name specified for a language can be any string.</span></span> <span data-ttu-id="7b4df-113">Por exemplo, o seguinte pode ser usado para definir o inglês dos EUA:</span><span class="sxs-lookup"><span data-stu-id="7b4df-113">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



<span data-ttu-id="7b4df-114">Se nenhum idioma SAMI for especificado, o primeiro idioma definido no arquivo SAMI será usado por padrão.</span><span class="sxs-lookup"><span data-stu-id="7b4df-114">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="7b4df-115">O valor que você passa usando *ClosedCaption*. **SAMILang** deve corresponder ao atributo **Name** no especificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="7b4df-115">The value you pass using *ClosedCaption*.**SAMILang** must match the **Name** attribute in the language specifier.</span></span>

<span data-ttu-id="7b4df-116">**Windows Media Player 10 Mobile:** Essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="7b4df-116">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="7b4df-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7b4df-117">Examples</span></span>

<span data-ttu-id="7b4df-118">O exemplo de JScript a seguir usa *ClosedCaption*. **SAMILang** em um elemento HTML SELECT para especificar a linguagem de legenda oculta.</span><span class="sxs-lookup"><span data-stu-id="7b4df-118">The following JScript example uses *ClosedCaption*.**SAMILang** in an HTML SELECT element to specify the closed caption language.</span></span> <span data-ttu-id="7b4df-119">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="7b4df-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="7b4df-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b4df-120">Requirements</span></span>



| <span data-ttu-id="7b4df-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b4df-121">Requirement</span></span> | <span data-ttu-id="7b4df-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7b4df-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4df-123">Versão</span><span class="sxs-lookup"><span data-stu-id="7b4df-123">Version</span></span><br/> | <span data-ttu-id="7b4df-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7b4df-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7b4df-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7b4df-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7b4df-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b4df-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b4df-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b4df-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4df-128">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="7b4df-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="7b4df-129">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="7b4df-129">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





