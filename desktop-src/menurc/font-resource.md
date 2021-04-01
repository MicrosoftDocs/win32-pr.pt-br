---
title: Recurso de fonte
description: Define um arquivo que contém uma fonte.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- Menus de recursos de fonte e outros recursos
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e205d80779a1a228ee50e062f6904c1ed4a4934
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638648"
---
# <a name="font-resource"></a><span data-ttu-id="a0ac1-104">Recurso de fonte</span><span class="sxs-lookup"><span data-stu-id="a0ac1-104">FONT resource</span></span>

<span data-ttu-id="a0ac1-105">Define um arquivo que contém uma fonte.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-105">Defines a file that contains a font.</span></span>

``` syntax
nameID FONT filename
```

## <a name="parameters"></a><span data-ttu-id="a0ac1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0ac1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0ac1-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="a0ac1-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="a0ac1-108">Valor inteiro sem sinal de 16 bits que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-108">Unique 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a0ac1-109"><span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="a0ac1-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="a0ac1-110">Nome do arquivo que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="a0ac1-111">O nome deve ser um nome de arquivo válido; Ele deve ser um caminho completo se o arquivo não estiver no diretório de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="a0ac1-112">O caminho deve ser uma cadeia de caracteres entre aspas.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="a0ac1-113">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="a0ac1-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="a0ac1-114">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="a0ac1-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a0ac1-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a0ac1-115">Examples</span></span>

<span data-ttu-id="a0ac1-116">O exemplo a seguir define um único recurso de fonte:</span><span class="sxs-lookup"><span data-stu-id="a0ac1-116">The following example defines a single font resource:</span></span>

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




