---
title: Ambiente. tabStop
description: O atributo tabStop especifica ou recupera um valor que indica se o controle está na ordem de tabulação. Você define a ordem de tabulação colocando o controle no script geral antes ou depois de outras marcas de controle.
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- Windows Media Player de ambiente. tabStop
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4005fc26a2bc5f928cde0f5ed67ec2098cf3e6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763380"
---
# <a name="ambientattributestabstop"></a><span data-ttu-id="5a138-105">Ambiente. tabStop</span><span class="sxs-lookup"><span data-stu-id="5a138-105">AmbientAttributes.tabStop</span></span>

<span data-ttu-id="5a138-106">O atributo **tabStop** especifica ou recupera um valor que indica se o controle está na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="5a138-106">The **tabStop** attribute specifies or retrieves a value indicating whether the control is in the tabbing order.</span></span> <span data-ttu-id="5a138-107">Você define a ordem de tabulação colocando o controle no script geral antes ou depois de outras marcas de controle.</span><span class="sxs-lookup"><span data-stu-id="5a138-107">You set the tabbing order by placing the control in the overall script before or after other control tags.</span></span>

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a><span data-ttu-id="5a138-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5a138-108">Possible Values</span></span>

<span data-ttu-id="5a138-109">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5a138-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="5a138-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5a138-110">Value</span></span> | <span data-ttu-id="5a138-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a138-111">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a138-112">true</span><span class="sxs-lookup"><span data-stu-id="5a138-112">true</span></span>  | <span data-ttu-id="5a138-113">O controle está na ordem de tabulação (o controle terá uma parada de tabulação: requisito de acessibilidade).</span><span class="sxs-lookup"><span data-stu-id="5a138-113">Control is in the tabbing order (control will have a tab stop: accessibility requirement).</span></span> |
| <span data-ttu-id="5a138-114">false</span><span class="sxs-lookup"><span data-stu-id="5a138-114">false</span></span> | <span data-ttu-id="5a138-115">O controle não está na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="5a138-115">Control is not in the tabbing order.</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="5a138-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a138-116">Remarks</span></span>

<span data-ttu-id="5a138-117">O atributo **tabStop** não é aplicável ao elemento **Effects** .</span><span class="sxs-lookup"><span data-stu-id="5a138-117">The **tabStop** attribute is not applicable to the **EFFECTS** element.</span></span>

<span data-ttu-id="5a138-118">O valor padrão para esse atributo é true para todos os elementos, exceto **menu** e **texto**, que têm um valor padrão de false.</span><span class="sxs-lookup"><span data-stu-id="5a138-118">The default value for this attribute is true for all elements except **AUTOMENU** and **TEXT**, which have a default value of false.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a138-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a138-119">Requirements</span></span>



| <span data-ttu-id="5a138-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a138-120">Requirement</span></span> | <span data-ttu-id="5a138-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5a138-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5a138-122">Versão</span><span class="sxs-lookup"><span data-stu-id="5a138-122">Version</span></span><br/> | <span data-ttu-id="5a138-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5a138-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a138-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a138-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a138-125">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="5a138-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





