---
title: FontFace de edição
description: O atributo fontFace especifica ou recupera a fonte para texto no controle da caixa de edição.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- Admy. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770503"
---
# <a name="editboxfontface"></a><span data-ttu-id="81ad6-104">FontFace de edição</span><span class="sxs-lookup"><span data-stu-id="81ad6-104">EDITBOX.fontFace</span></span>

<span data-ttu-id="81ad6-105">O atributo **fontface** especifica ou recupera a fonte para texto no controle da caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="81ad6-105">The **fontFace** attribute specifies or retrieves the font for text in the edit box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="81ad6-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="81ad6-106">Possible Values</span></span>

<span data-ttu-id="81ad6-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="81ad6-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="81ad6-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="81ad6-108">Remarks</span></span>

<span data-ttu-id="81ad6-109">Esse atributo pode ser o nome de qualquer fonte válida disponível no Windows.</span><span class="sxs-lookup"><span data-stu-id="81ad6-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="81ad6-110">O Windows Media Player não oferecerá suporte à instalação de fontes, portanto, escolha uma fonte que você sabe que estará no sistema pretendido.</span><span class="sxs-lookup"><span data-stu-id="81ad6-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="81ad6-111">Se o **fontface** especificado não estiver disponível no sistema do usuário, o controle caixa de edição usa como padrão a fonte do sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="81ad6-111">If the **fontFace** specified is not available on the user's system, the edit box control defaults to the Windows system font.</span></span> <span data-ttu-id="81ad6-112">O valor padrão para sistemas de idioma inglês é "Tahoma".</span><span class="sxs-lookup"><span data-stu-id="81ad6-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="81ad6-113">Para sistemas internacionais, o padrão é carregado a partir de um arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="81ad6-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="81ad6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81ad6-114">Requirements</span></span>



| <span data-ttu-id="81ad6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="81ad6-115">Requirement</span></span> | <span data-ttu-id="81ad6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="81ad6-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="81ad6-117">Versão</span><span class="sxs-lookup"><span data-stu-id="81ad6-117">Version</span></span><br/> | <span data-ttu-id="81ad6-118">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="81ad6-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81ad6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="81ad6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ad6-120">**Elemento admy**</span><span class="sxs-lookup"><span data-stu-id="81ad6-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="81ad6-121">**Mythe. fontSize**</span><span class="sxs-lookup"><span data-stu-id="81ad6-121">**EDITBOX.fontSize**</span></span>](editbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="81ad6-122">**FontStyle de edição**</span><span class="sxs-lookup"><span data-stu-id="81ad6-122">**EDITBOX.fontStyle**</span></span>](editbox-fontstyle.md)
</dt> </dl>

 

 





