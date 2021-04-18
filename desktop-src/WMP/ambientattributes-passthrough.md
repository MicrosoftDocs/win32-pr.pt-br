---
title: Ambiente de passagem. passThrough
description: O atributo passThrough especifica ou recupera um valor que indica se o controle passará todos os eventos do mouse para o controle sob ele.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- Windows Media Player de ambiente. passThrough
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763381"
---
# <a name="ambientattributespassthrough"></a><span data-ttu-id="4d040-104">Ambiente de passagem. passThrough</span><span class="sxs-lookup"><span data-stu-id="4d040-104">AmbientAttributes.passThrough</span></span>

<span data-ttu-id="4d040-105">O atributo **passThrough** especifica ou recupera um valor que indica se o controle passará todos os eventos do mouse para o controle sob ele.</span><span class="sxs-lookup"><span data-stu-id="4d040-105">The **passThrough** attribute specifies or retrieves a value indicating whether the control will pass all mouse events through to the control under it.</span></span>

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a><span data-ttu-id="4d040-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="4d040-106">Possible Values</span></span>

<span data-ttu-id="4d040-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4d040-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="4d040-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4d040-108">Value</span></span> | <span data-ttu-id="4d040-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d040-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="4d040-110">true</span><span class="sxs-lookup"><span data-stu-id="4d040-110">true</span></span>  | <span data-ttu-id="4d040-111">O controle passa eventos para o controle sob ele.</span><span class="sxs-lookup"><span data-stu-id="4d040-111">Control passes events through to the control under it.</span></span> |
| <span data-ttu-id="4d040-112">false</span><span class="sxs-lookup"><span data-stu-id="4d040-112">false</span></span> | <span data-ttu-id="4d040-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="4d040-113">Default.</span></span> <span data-ttu-id="4d040-114">O controle não passa eventos pelo.</span><span class="sxs-lookup"><span data-stu-id="4d040-114">Control does not pass events through.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="4d040-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d040-115">Remarks</span></span>

<span data-ttu-id="4d040-116">Esse atributo será útil se, por exemplo, um controle de texto estiver sobre um controle de botão apenas para fornecer rotulagem.</span><span class="sxs-lookup"><span data-stu-id="4d040-116">This attribute is useful if, for example, a text control sits on top of a button control only to provide labeling.</span></span> <span data-ttu-id="4d040-117">Nesse caso, os cliques no controle de texto devem ser passados para o controle de botão.</span><span class="sxs-lookup"><span data-stu-id="4d040-117">In this case, clicks on the text control must be passed through to the button control.</span></span>

<span data-ttu-id="4d040-118">Não há suporte para o atributo **passThrough** nos elementos **VIEW**, **subview** e **playlist** .</span><span class="sxs-lookup"><span data-stu-id="4d040-118">The **passThrough** attribute is not supported by the **VIEW**, **SUBVIEW**, and **PLAYLIST** elements.</span></span> <span data-ttu-id="4d040-119">Ele não funcionará com o elemento **Video** se for um *vídeo*. **sem janela** é definido como false, nem com o elemento **Effects** , se houver *efeitos*. em **janela** é definido como true.</span><span class="sxs-lookup"><span data-stu-id="4d040-119">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d040-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d040-120">Requirements</span></span>



| <span data-ttu-id="4d040-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d040-121">Requirement</span></span> | <span data-ttu-id="4d040-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4d040-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4d040-123">Versão</span><span class="sxs-lookup"><span data-stu-id="4d040-123">Version</span></span><br/> | <span data-ttu-id="4d040-124">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4d040-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d040-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d040-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d040-126">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="4d040-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





