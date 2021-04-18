---
title: Elemento Color
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento Color
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Elemento Color do Windows Media Player
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c73aa9fe2c7f731e872c4a2e235bf9c0e29ce05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813369"
---
# <a name="color-element"></a><span data-ttu-id="8b425-105">Elemento Color</span><span class="sxs-lookup"><span data-stu-id="8b425-105">Color Element</span></span>

> [!Note]  
> <span data-ttu-id="8b425-106">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="8b425-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="8b425-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="8b425-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="8b425-108">O elemento Color especifica a cor do plano de fundo dos botões de navegação da loja online, do texto do botão e da barra de tarefas recursos.</span><span class="sxs-lookup"><span data-stu-id="8b425-108">The Color element specifies the background color for online store navigation buttons, button text, and the Features taskbar.</span></span>

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a><span data-ttu-id="8b425-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="8b425-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="8b425-110"><span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="8b425-110"><span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (required)</span></span>
</dt> <dd>

<span data-ttu-id="8b425-111">Valor de cor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="8b425-111">Hexadecimal RGB color value.</span></span> <span data-ttu-id="8b425-112">Especifica a cor do plano de fundo dos botões e da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="8b425-112">Specifies the background color for buttons and the taskbar.</span></span>

</dd> <dt>

<span data-ttu-id="8b425-113"><span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="8b425-113"><span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (required)</span></span>
</dt> <dd>

<span data-ttu-id="8b425-114">Valor de cor RGB hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="8b425-114">Hexadecimal RGB color value.</span></span> <span data-ttu-id="8b425-115">Especifica a cor do texto do botão.</span><span class="sxs-lookup"><span data-stu-id="8b425-115">Specifies the color for the button text.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="8b425-116">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="8b425-116">Parent/Child Elements</span></span>



| <span data-ttu-id="8b425-117">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="8b425-117">Hierarchy</span></span>       | <span data-ttu-id="8b425-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="8b425-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="8b425-119">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8b425-119">Parent elements</span></span> | <span data-ttu-id="8b425-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="8b425-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="8b425-121">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8b425-121">Child elements</span></span>  | <span data-ttu-id="8b425-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8b425-122">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="8b425-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b425-123">Remarks</span></span>

<span data-ttu-id="8b425-124">O valor padrão para **MediaPlayer** é \# 7C9AD6.</span><span class="sxs-lookup"><span data-stu-id="8b425-124">The default value for **MediaPlayer** is \#7C9AD6.</span></span> <span data-ttu-id="8b425-125">O valor padrão para **MediaPlayerText** é \# FFFFFF.</span><span class="sxs-lookup"><span data-stu-id="8b425-125">The default value for **MediaPlayerText** is \#FFFFFF.</span></span>

<span data-ttu-id="8b425-126">Certifique-se de usar cores que tornam mais fácil para o usuário ler o texto do botão.</span><span class="sxs-lookup"><span data-stu-id="8b425-126">Be sure to use colors that make it easy for the user to read the button text.</span></span> <span data-ttu-id="8b425-127">Por exemplo, você deve evitar o uso de texto de botão branco em botões de cor clara.</span><span class="sxs-lookup"><span data-stu-id="8b425-127">For example, you should avoid using white button text on light colored buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b425-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b425-128">Requirements</span></span>



| <span data-ttu-id="8b425-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b425-129">Requirement</span></span> | <span data-ttu-id="8b425-130">Valor</span><span class="sxs-lookup"><span data-stu-id="8b425-130">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="8b425-131">Versão</span><span class="sxs-lookup"><span data-stu-id="8b425-131">Version</span></span><br/> | <span data-ttu-id="8b425-132">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8b425-132">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b425-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b425-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b425-134">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="8b425-134">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="8b425-135">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="8b425-135">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="8b425-136">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="8b425-136">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





