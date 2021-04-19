---
title: TEXT. toolTip
description: O atributo toolTip especifica ou recupera o texto da dica de ferramenta para o controle de texto.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- TEXT. toolTip Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770124"
---
# <a name="texttooltip"></a><span data-ttu-id="92a18-104">TEXT. toolTip</span><span class="sxs-lookup"><span data-stu-id="92a18-104">TEXT.toolTip</span></span>

<span data-ttu-id="92a18-105">O atributo **ToolTip** especifica ou recupera o texto da dica de ferramenta para o controle de texto.</span><span class="sxs-lookup"><span data-stu-id="92a18-105">The **toolTip** attribute specifies or retrieves the ToolTip text for the text control.</span></span>

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a><span data-ttu-id="92a18-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="92a18-106">Possible Values</span></span>

<span data-ttu-id="92a18-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação com um comprimento máximo de 1024 caracteres.</span><span class="sxs-lookup"><span data-stu-id="92a18-107">This attribute is a read/write **String** with a maximum length of 1024 characters.</span></span> <span data-ttu-id="92a18-108">Não tem nenhum valor padrão.</span><span class="sxs-lookup"><span data-stu-id="92a18-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92a18-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="92a18-109">Remarks</span></span>

<span data-ttu-id="92a18-110">Se esse atributo não for especificado e o texto no atributo de **valor** estiver truncado no controle de texto, ou se **WordWrap** for definido como true, a dica de ferramenta exibirá o texto completo do atributo **Value** .</span><span class="sxs-lookup"><span data-stu-id="92a18-110">If this attribute is not specified, and the text in the **value** attribute is truncated in the Text control, or **wordWrap** is set to true, the ToolTip will display the full text of the **value** attribute.</span></span>

<span data-ttu-id="92a18-111">Quando esse atributo é definido como "" (cadeia de caracteres vazia), nenhuma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="92a18-111">When this attribute is set to "" (empty string), no ToolTip is displayed.</span></span>

<span data-ttu-id="92a18-112">Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.</span><span class="sxs-lookup"><span data-stu-id="92a18-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="92a18-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92a18-113">Requirements</span></span>



| <span data-ttu-id="92a18-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="92a18-114">Requirement</span></span> | <span data-ttu-id="92a18-115">Valor</span><span class="sxs-lookup"><span data-stu-id="92a18-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="92a18-116">Versão</span><span class="sxs-lookup"><span data-stu-id="92a18-116">Version</span></span><br/> | <span data-ttu-id="92a18-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="92a18-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92a18-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="92a18-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a18-119">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="92a18-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="92a18-120">**TEXT. Value**</span><span class="sxs-lookup"><span data-stu-id="92a18-120">**TEXT.value**</span></span>](text-value.md)
</dt> <dt>

[<span data-ttu-id="92a18-121">**TEXT. wordWrap**</span><span class="sxs-lookup"><span data-stu-id="92a18-121">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





