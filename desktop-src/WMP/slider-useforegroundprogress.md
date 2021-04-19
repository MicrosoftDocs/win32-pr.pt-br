---
title: SLIDER. useForegroundProgress
description: O atributo useForegroundProgress especifica ou recupera um valor que indica se a barra de progresso de primeiro plano será usada.
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- Controle deslizante. useForegroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b572933549417713158acea1a24fa9e1434c9dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749397"
---
# <a name="slideruseforegroundprogress"></a><span data-ttu-id="47e49-104">SLIDER. useForegroundProgress</span><span class="sxs-lookup"><span data-stu-id="47e49-104">SLIDER.useForegroundProgress</span></span>

<span data-ttu-id="47e49-105">O atributo **useForegroundProgress** especifica ou recupera um valor que indica se a barra de progresso de primeiro plano será usada.</span><span class="sxs-lookup"><span data-stu-id="47e49-105">The **useForegroundProgress** attribute specifies or retrieves a value indicating whether the foreground progress bar will be used.</span></span>

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="47e49-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="47e49-106">Possible Values</span></span>

<span data-ttu-id="47e49-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="47e49-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="47e49-108">Valor</span><span class="sxs-lookup"><span data-stu-id="47e49-108">Value</span></span> | <span data-ttu-id="47e49-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="47e49-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="47e49-110">true</span><span class="sxs-lookup"><span data-stu-id="47e49-110">true</span></span>  | <span data-ttu-id="47e49-111">Use o andamento do primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="47e49-111">Use foreground progress.</span></span>                 |
| <span data-ttu-id="47e49-112">false</span><span class="sxs-lookup"><span data-stu-id="47e49-112">false</span></span> | <span data-ttu-id="47e49-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="47e49-113">Default.</span></span> <span data-ttu-id="47e49-114">Não use o progresso em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="47e49-114">Do not use foreground progress.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="47e49-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="47e49-115">Remarks</span></span>

<span data-ttu-id="47e49-116">Esse atributo permite o uso do atributo **foregroundProgress** , que é usado principalmente para acompanhar o progresso do download de um arquivo de mídia enquanto controla simultaneamente a posição de execução atual do arquivo usando o atributo **Value** .</span><span class="sxs-lookup"><span data-stu-id="47e49-116">This attribute allows the use of the **foregroundProgress** attribute, which is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="47e49-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47e49-117">Requirements</span></span>



| <span data-ttu-id="47e49-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="47e49-118">Requirement</span></span> | <span data-ttu-id="47e49-119">Valor</span><span class="sxs-lookup"><span data-stu-id="47e49-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="47e49-120">Versão</span><span class="sxs-lookup"><span data-stu-id="47e49-120">Version</span></span><br/> | <span data-ttu-id="47e49-121">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="47e49-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47e49-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="47e49-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e49-123">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="47e49-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="47e49-124">**SLIDER. foregroundProgress**</span><span class="sxs-lookup"><span data-stu-id="47e49-124">**SLIDER.foregroundProgress**</span></span>](slider-foregroundprogress.md)
</dt> <dt>

[<span data-ttu-id="47e49-125">**Controle deslizante. valor**</span><span class="sxs-lookup"><span data-stu-id="47e49-125">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





