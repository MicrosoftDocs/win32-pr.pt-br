---
title: TEXT. fontFace
description: O atributo fontFace especifica ou recupera o tipo de fonte para o controle de texto.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- TEXT. fontFace Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183b25547e456cb90cac4d2137354679e13d8a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771649"
---
# <a name="textfontface"></a><span data-ttu-id="2696a-104">TEXT. fontFace</span><span class="sxs-lookup"><span data-stu-id="2696a-104">TEXT.fontFace</span></span>

<span data-ttu-id="2696a-105">O atributo **fontface** especifica ou recupera o tipo de fonte para o controle de texto.</span><span class="sxs-lookup"><span data-stu-id="2696a-105">The **fontFace** attribute specifies or retrieves the typeface for the Text control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="2696a-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="2696a-106">Possible Values</span></span>

<span data-ttu-id="2696a-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2696a-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2696a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="2696a-108">Remarks</span></span>

<span data-ttu-id="2696a-109">Esse atributo pode ser o nome de qualquer fonte válida disponível no Windows.</span><span class="sxs-lookup"><span data-stu-id="2696a-109">This attribute can be the name of any valid font available on Windows.</span></span> <span data-ttu-id="2696a-110">O Windows Media Player não oferecerá suporte à instalação de fontes, portanto, escolha uma fonte que você sabe que estará no sistema pretendido.</span><span class="sxs-lookup"><span data-stu-id="2696a-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="2696a-111">Se o **fontface** especificado não estiver disponível no sistema do usuário, o controle de texto usa como padrão a fonte do sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="2696a-111">If the **fontFace** specified is not available on the user's system, the Text control defaults to the Windows system font.</span></span>

<span data-ttu-id="2696a-112">Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.</span><span class="sxs-lookup"><span data-stu-id="2696a-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2696a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2696a-113">Requirements</span></span>



| <span data-ttu-id="2696a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2696a-114">Requirement</span></span> | <span data-ttu-id="2696a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2696a-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2696a-116">Versão</span><span class="sxs-lookup"><span data-stu-id="2696a-116">Version</span></span><br/> | <span data-ttu-id="2696a-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="2696a-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2696a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="2696a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2696a-119">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="2696a-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="2696a-120">**TEXT. fontSize**</span><span class="sxs-lookup"><span data-stu-id="2696a-120">**TEXT.fontSize**</span></span>](text-fontsize.md)
</dt> </dl>

 

 





