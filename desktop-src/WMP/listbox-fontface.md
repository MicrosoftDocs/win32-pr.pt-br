---
title: LISTBOX. fontFace
description: O atributo fontFace especifica ou recupera a fonte do controle de caixa de listagem.
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- LISTBOX. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796135"
---
# <a name="listboxfontface"></a><span data-ttu-id="17c53-104">LISTBOX. fontFace</span><span class="sxs-lookup"><span data-stu-id="17c53-104">LISTBOX.fontFace</span></span>

<span data-ttu-id="17c53-105">O atributo **fontface** especifica ou recupera a fonte do controle de caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="17c53-105">The **fontFace** attribute specifies or retrieves the font for the list box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="17c53-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="17c53-106">Possible Values</span></span>

<span data-ttu-id="17c53-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="17c53-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="17c53-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="17c53-108">Remarks</span></span>

<span data-ttu-id="17c53-109">Esse atributo pode ser o nome de qualquer fonte válida disponível no Windows.</span><span class="sxs-lookup"><span data-stu-id="17c53-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="17c53-110">O Windows Media Player não oferecerá suporte à instalação de fontes, portanto, escolha uma fonte que você sabe que estará no sistema pretendido.</span><span class="sxs-lookup"><span data-stu-id="17c53-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="17c53-111">Se o **fontface** especificado não estiver disponível no sistema do usuário, o controle caixa de listagem usa como padrão a fonte do sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="17c53-111">If the **fontFace** specified is not available on the user's system, the list box control defaults to the Windows system font.</span></span> <span data-ttu-id="17c53-112">O valor padrão para sistemas de idioma inglês é "Tahoma".</span><span class="sxs-lookup"><span data-stu-id="17c53-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="17c53-113">Para sistemas internacionais, o padrão é carregado a partir de um arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="17c53-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="17c53-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17c53-114">Requirements</span></span>



| <span data-ttu-id="17c53-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="17c53-115">Requirement</span></span> | <span data-ttu-id="17c53-116">Valor</span><span class="sxs-lookup"><span data-stu-id="17c53-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="17c53-117">Versão</span><span class="sxs-lookup"><span data-stu-id="17c53-117">Version</span></span><br/> | <span data-ttu-id="17c53-118">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="17c53-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17c53-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="17c53-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c53-120">**Elemento LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="17c53-120">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="17c53-121">**Caixa de listagem. fontSize**</span><span class="sxs-lookup"><span data-stu-id="17c53-121">**LISTBOX.fontSize**</span></span>](listbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="17c53-122">**LISTBOX. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="17c53-122">**LISTBOX.fontStyle**</span></span>](listbox-fontstyle.md)
</dt> </dl>

 

 





