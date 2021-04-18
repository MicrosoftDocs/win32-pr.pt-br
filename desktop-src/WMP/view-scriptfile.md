---
title: Exibir. scriptfile
description: O atributo scriptfile especifica os nomes de arquivo que acompanham arquivos JScript.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- Exibir. scriptfile Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751923"
---
# <a name="viewscriptfile"></a><span data-ttu-id="f273d-104">Exibir. scriptfile</span><span class="sxs-lookup"><span data-stu-id="f273d-104">VIEW.scriptFile</span></span>

<span data-ttu-id="f273d-105">O atributo **scriptfile** especifica os nomes de arquivo que acompanham arquivos JScript.</span><span class="sxs-lookup"><span data-stu-id="f273d-105">The **scriptFile** attribute specifies the file names of accompanying JScript files.</span></span>

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a><span data-ttu-id="f273d-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="f273d-106">Possible Values</span></span>

<span data-ttu-id="f273d-107">Esse atributo é uma **cadeia de caracteres** somente gravação sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="f273d-107">This attribute is a write-only **String** with no default value.</span></span> <span data-ttu-id="f273d-108">Os nomes de arquivo de vários arquivos JScript são delimitados por ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="f273d-108">The file names of multiple JScript files are delimited with semicolons.</span></span> <span data-ttu-id="f273d-109">Os espaços e pontos e vírgulas iniciais e seguintes não devem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="f273d-109">Leading and following spaces and semicolons should not be present.</span></span>

## <a name="remarks"></a><span data-ttu-id="f273d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f273d-110">Remarks</span></span>

<span data-ttu-id="f273d-111">O código nos arquivos especificados pode ser usado por qualquer manipulador de eventos na exibição.</span><span class="sxs-lookup"><span data-stu-id="f273d-111">The code in the specified files can be used by any event handler in the View.</span></span> <span data-ttu-id="f273d-112">O código usado por manipuladores de eventos em várias exibições pode ser colocado em um arquivo com o mesmo nome do arquivo de definição de capa, mas com uma extensão. js em vez de uma extensão. WMS.</span><span class="sxs-lookup"><span data-stu-id="f273d-112">Code that is used by event handlers in multiple Views can be placed in a file with the same name as the skin definition file but with a .js extension instead of a .wms extension.</span></span> <span data-ttu-id="f273d-113">Esse arquivo é carregado automaticamente e não precisa ser especificado no arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="f273d-113">This file is loaded automatically and need not be specified in the skin definition file.</span></span>

## <a name="examples"></a><span data-ttu-id="f273d-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f273d-114">Examples</span></span>


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a><span data-ttu-id="f273d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f273d-115">Requirements</span></span>



| <span data-ttu-id="f273d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f273d-116">Requirement</span></span> | <span data-ttu-id="f273d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f273d-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f273d-118">Versão</span><span class="sxs-lookup"><span data-stu-id="f273d-118">Version</span></span><br/> | <span data-ttu-id="f273d-119">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f273d-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f273d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="f273d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f273d-121">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="f273d-121">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





