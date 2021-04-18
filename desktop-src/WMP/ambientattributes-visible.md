---
title: Ambienteattributes. visível
description: O atributo Visible especifica ou recupera a visibilidade do controle.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- Ambiente do Windows Media Player visível.
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762108"
---
# <a name="ambientattributesvisible"></a><span data-ttu-id="335a5-104">Ambienteattributes. visível</span><span class="sxs-lookup"><span data-stu-id="335a5-104">AmbientAttributes.visible</span></span>

<span data-ttu-id="335a5-105">O atributo **Visible** especifica ou recupera a visibilidade do controle.</span><span class="sxs-lookup"><span data-stu-id="335a5-105">The **visible** attribute specifies or retrieves the visibility for the control.</span></span>

``` syntax
        elementID.visible
```

## <a name="possible-values"></a><span data-ttu-id="335a5-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="335a5-106">Possible Values</span></span>

<span data-ttu-id="335a5-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="335a5-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="335a5-108">Valor</span><span class="sxs-lookup"><span data-stu-id="335a5-108">Value</span></span> | <span data-ttu-id="335a5-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="335a5-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="335a5-110">true</span><span class="sxs-lookup"><span data-stu-id="335a5-110">true</span></span>  | <span data-ttu-id="335a5-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="335a5-111">Default.</span></span> <span data-ttu-id="335a5-112">O controle é visível.</span><span class="sxs-lookup"><span data-stu-id="335a5-112">The control is visible.</span></span> |
| <span data-ttu-id="335a5-113">false</span><span class="sxs-lookup"><span data-stu-id="335a5-113">false</span></span> | <span data-ttu-id="335a5-114">O controle não está visível.</span><span class="sxs-lookup"><span data-stu-id="335a5-114">The control is not visible.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="335a5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="335a5-115">Remarks</span></span>

<span data-ttu-id="335a5-116">Esse atributo é útil para ocultar controles, por exemplo, ao alternar um botão de pausa para um botão de reprodução.</span><span class="sxs-lookup"><span data-stu-id="335a5-116">This attribute is useful for hiding controls, for example when swapping a pause button for a play button.</span></span>

<span data-ttu-id="335a5-117">Se o valor for false, o controle não será visível e os eventos de clique serão passados para o controle por trás dele.</span><span class="sxs-lookup"><span data-stu-id="335a5-117">If the value is false, the control is not visible and click events are passed to the control behind it.</span></span> <span data-ttu-id="335a5-118">Se o valor for true, o controle ficará visível e receberá o próprio evento de clique.</span><span class="sxs-lookup"><span data-stu-id="335a5-118">If the value is true, the control is visible and receives the click event itself.</span></span>

<span data-ttu-id="335a5-119">O valor padrão para o elemento **Automenu** é false.</span><span class="sxs-lookup"><span data-stu-id="335a5-119">The default value for the **AUTOMENU** element is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="335a5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="335a5-120">Requirements</span></span>



| <span data-ttu-id="335a5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="335a5-121">Requirement</span></span> | <span data-ttu-id="335a5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="335a5-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="335a5-123">Versão</span><span class="sxs-lookup"><span data-stu-id="335a5-123">Version</span></span><br/> | <span data-ttu-id="335a5-124">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="335a5-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="335a5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="335a5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="335a5-126">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="335a5-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





