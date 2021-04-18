---
title: Exibir. titleBar
description: O atributo titleBar recupera um valor que indica se a barra de título da janela é mostrada.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- Exibir. titleBar Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea225103913e3906cf6cd3b129943fbf9b9f165
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788640"
---
# <a name="viewtitlebar"></a><span data-ttu-id="46a79-104">Exibir. titleBar</span><span class="sxs-lookup"><span data-stu-id="46a79-104">VIEW.titleBar</span></span>

<span data-ttu-id="46a79-105">O atributo **TitleBar** recupera um valor que indica se a barra de título da janela é mostrada.</span><span class="sxs-lookup"><span data-stu-id="46a79-105">The **titleBar** attribute retrieves a value indicating whether the window title bar is shown.</span></span>

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a><span data-ttu-id="46a79-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="46a79-106">Possible Values</span></span>

<span data-ttu-id="46a79-107">Esse atributo é um **booliano** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="46a79-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="46a79-108">Valor</span><span class="sxs-lookup"><span data-stu-id="46a79-108">Value</span></span> | <span data-ttu-id="46a79-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="46a79-109">Description</span></span>                             |
|-------|-----------------------------------------|
| <span data-ttu-id="46a79-110">true</span><span class="sxs-lookup"><span data-stu-id="46a79-110">true</span></span>  | <span data-ttu-id="46a79-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="46a79-111">Default.</span></span> <span data-ttu-id="46a79-112">A barra de título da janela é mostrada.</span><span class="sxs-lookup"><span data-stu-id="46a79-112">The window title bar is shown.</span></span> |
| <span data-ttu-id="46a79-113">false</span><span class="sxs-lookup"><span data-stu-id="46a79-113">false</span></span> | <span data-ttu-id="46a79-114">A barra de título da janela não é mostrada.</span><span class="sxs-lookup"><span data-stu-id="46a79-114">The window title bar is not shown.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="46a79-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="46a79-115">Remarks</span></span>

<span data-ttu-id="46a79-116">Se a barra de título for mostrada, os botões caixa de controle, minimizar e fechar serão mostrados.</span><span class="sxs-lookup"><span data-stu-id="46a79-116">If the title bar is shown, the control box, minimize, and close buttons will be shown.</span></span> <span data-ttu-id="46a79-117">O título da janela será o título do elemento de **exibição** .</span><span class="sxs-lookup"><span data-stu-id="46a79-117">The title of the window will be the title of the **VIEW** element.</span></span>

<span data-ttu-id="46a79-118">Se **TitleBar** estiver definido como true e o usuário tentar alterar o valor de **video. Zoom**, a alteração não ocorrerá a menos que a capa monitore o **zoom** e tome a medida apropriada para se redimensionar.</span><span class="sxs-lookup"><span data-stu-id="46a79-118">If **titleBar** is set to true and the user attempts to change the value of **Video.zoom**, the change will not take place unless the skin monitors **zoom** and takes appropriate action to resize itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="46a79-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46a79-119">Requirements</span></span>



| <span data-ttu-id="46a79-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="46a79-120">Requirement</span></span> | <span data-ttu-id="46a79-121">Valor</span><span class="sxs-lookup"><span data-stu-id="46a79-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="46a79-122">Versão</span><span class="sxs-lookup"><span data-stu-id="46a79-122">Version</span></span><br/> | <span data-ttu-id="46a79-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="46a79-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46a79-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="46a79-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46a79-125">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="46a79-125">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="46a79-126">**Exibir. title**</span><span class="sxs-lookup"><span data-stu-id="46a79-126">**VIEW.title**</span></span>](view-title.md)
</dt> <dt>

[<span data-ttu-id="46a79-127">**VIDEO. zoom**</span><span class="sxs-lookup"><span data-stu-id="46a79-127">**VIDEO.zoom**</span></span>](video-zoom.md)
</dt> </dl>

 

 





