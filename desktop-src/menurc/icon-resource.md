---
title: Recurso de ícone
description: Define um bitmap que define a forma do ícone a ser usado para um determinado aplicativo ou um ícone animado.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- ÍCONE de menus de recursos e outros recursos
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499026"
---
# <a name="icon-resource"></a><span data-ttu-id="7f591-104">Recurso de ícone</span><span class="sxs-lookup"><span data-stu-id="7f591-104">ICON resource</span></span>

<span data-ttu-id="7f591-105">Define um bitmap que define a forma do ícone a ser usado para um determinado aplicativo ou um ícone animado.</span><span class="sxs-lookup"><span data-stu-id="7f591-105">Defines a bitmap that defines the shape of the icon to be used for a given application or an animated icon.</span></span>

``` syntax
nameID ICON filename
```

## <a name="parameters"></a><span data-ttu-id="7f591-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f591-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f591-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="7f591-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="7f591-108">Nome exclusivo ou um valor inteiro sem sinal de 16 bits que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="7f591-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="7f591-109"><span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="7f591-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="7f591-110">Nome do arquivo que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="7f591-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="7f591-111">O nome deve ser um nome de arquivo válido; Ele deve ser um caminho completo se o arquivo não estiver no diretório de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="7f591-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="7f591-112">O caminho deve ser uma cadeia de caracteres entre aspas.</span><span class="sxs-lookup"><span data-stu-id="7f591-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="7f591-113">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="7f591-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="7f591-114">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="7f591-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7f591-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f591-115">Remarks</span></span>

<span data-ttu-id="7f591-116">Os recursos de ícone e cursor podem conter mais de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7f591-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="7f591-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7f591-117">Examples</span></span>

<span data-ttu-id="7f591-118">O exemplo a seguir define dois recursos de ícone:</span><span class="sxs-lookup"><span data-stu-id="7f591-118">The following example defines two icon resources:</span></span>

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a><span data-ttu-id="7f591-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f591-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f591-120">Usando ícones</span><span class="sxs-lookup"><span data-stu-id="7f591-120">Using Icons</span></span>](./using-icons.md)
</dt> </dl>

 

 