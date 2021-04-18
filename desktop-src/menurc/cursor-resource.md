---
title: Recurso de CURSOR
description: Define um bitmap que define a forma do cursor na tela de exibição ou um cursor animado.
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- Menus de recursos de CURSOR e outros recursos
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105758708"
---
# <a name="cursor-resource"></a><span data-ttu-id="3a245-104">Recurso de CURSOR</span><span class="sxs-lookup"><span data-stu-id="3a245-104">CURSOR resource</span></span>

<span data-ttu-id="3a245-105">Define um bitmap que define a forma do cursor na tela de exibição ou um cursor animado.</span><span class="sxs-lookup"><span data-stu-id="3a245-105">Defines a bitmap that defines the shape of the cursor on the display screen or an animated cursor.</span></span>

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a><span data-ttu-id="3a245-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a245-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a245-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="3a245-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="3a245-108">Nome exclusivo ou um inteiro de 16 bits sem sinal identificando o recurso.</span><span class="sxs-lookup"><span data-stu-id="3a245-108">Unique name or a 16-bit unsigned integer identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="3a245-109"><span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="3a245-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="3a245-110">Nome do arquivo que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="3a245-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="3a245-111">O nome deve ser um nome de arquivo válido; Ele deve ser um caminho completo se o arquivo não estiver no diretório de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="3a245-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="3a245-112">O caminho deve ser uma cadeia de caracteres entre aspas.</span><span class="sxs-lookup"><span data-stu-id="3a245-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="3a245-113">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="3a245-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="3a245-114">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="3a245-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3a245-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a245-115">Remarks</span></span>

<span data-ttu-id="3a245-116">Os recursos de ícone e cursor podem conter mais de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="3a245-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="3a245-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3a245-117">Examples</span></span>

<span data-ttu-id="3a245-118">O exemplo a seguir define dois recursos de cursor; um por nome (cursor1) e o outro por número (2):</span><span class="sxs-lookup"><span data-stu-id="3a245-118">The following example defines two cursor resources; one by name (cursor1) and the other by number (2):</span></span>

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a><span data-ttu-id="3a245-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a245-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a245-120">Usando cursores</span><span class="sxs-lookup"><span data-stu-id="3a245-120">Using Cursors</span></span>](./using-cursors.md)
</dt> </dl>

 

 