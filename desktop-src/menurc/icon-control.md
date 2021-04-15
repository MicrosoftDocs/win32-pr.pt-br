---
title: Controle de ícone
description: Define um controle de ícone. Esse controle é um ícone exibido em uma caixa de diálogo.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Menus de controle de ícone e outros recursos
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400136395a17f039d552373fa35cba0f3545a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453765"
---
# <a name="icon-control"></a><span data-ttu-id="6d491-105">Controle de ícone</span><span class="sxs-lookup"><span data-stu-id="6d491-105">ICON control</span></span>

<span data-ttu-id="6d491-106">Define um controle de ícone.</span><span class="sxs-lookup"><span data-stu-id="6d491-106">Defines an icon control.</span></span> <span data-ttu-id="6d491-107">Esse controle é um ícone exibido em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6d491-107">This control is an icon displayed in a dialog box.</span></span>

<span data-ttu-id="6d491-108">A instrução de controle **Icon** , que pode ser usada apenas em uma instrução [**DIALOGEX**](dialogex-resource.md) , define o identificador de recurso de ícone, o identificador de controle de ícone, a posição e os atributos de um controle.</span><span class="sxs-lookup"><span data-stu-id="6d491-108">The **ICON** control statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the icon-resource identifier, icon-control identifier, position, and attributes of a control.</span></span>

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="6d491-109"><span id="text"></span><span id="TEXT"></span>*texto*</span><span class="sxs-lookup"><span data-stu-id="6d491-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="6d491-110">Nome de um ícone (não um nome de arquivo) definido em outro lugar no arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="6d491-110">Name of an icon (not a file name) defined elsewhere in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="6d491-111"><span id="width"></span><span id="WIDTH"></span>*Largura*</span><span class="sxs-lookup"><span data-stu-id="6d491-111"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="6d491-112">Esse valor é ignorado e deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="6d491-112">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6d491-113"><span id="height"></span><span id="HEIGHT"></span>*tamanho*</span><span class="sxs-lookup"><span data-stu-id="6d491-113"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="6d491-114">Esse valor é ignorado e deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="6d491-114">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6d491-115"><span id="style"></span><span id="STYLE"></span>*estilo*</span><span class="sxs-lookup"><span data-stu-id="6d491-115"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="6d491-116">Estilo de controle.</span><span class="sxs-lookup"><span data-stu-id="6d491-116">Control style.</span></span> <span data-ttu-id="6d491-117">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="6d491-117">This parameter is optional.</span></span> <span data-ttu-id="6d491-118">O único valor que pode ser especificado é o estilo de **\_ ícone SS** .</span><span class="sxs-lookup"><span data-stu-id="6d491-118">The only value that can be specified is the **SS\_ICON** style.</span></span> <span data-ttu-id="6d491-119">Esse é o estilo padrão se esse parâmetro é especificado ou não.</span><span class="sxs-lookup"><span data-stu-id="6d491-119">This is the default style whether this parameter is specified or not.</span></span>

</dd> </dl>

<span data-ttu-id="6d491-120">Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6d491-120">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6d491-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d491-121">Examples</span></span>

<span data-ttu-id="6d491-122">Este exemplo define um controle de ícone cujo identificador de ícone é 901 e cujo nome é myicon:</span><span class="sxs-lookup"><span data-stu-id="6d491-122">This example defines an icon control whose icon identifier is 901 and whose name is myicon:</span></span>

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a><span data-ttu-id="6d491-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d491-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d491-124">**CONE**</span><span class="sxs-lookup"><span data-stu-id="6d491-124">**ICON**</span></span>](icon-resource.md)
</dt> </dl>

 

 




