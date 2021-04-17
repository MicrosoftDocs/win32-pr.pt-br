---
description: Os objetos de dados contêm os dados reais ou uma referência a esses dados. Cada objeto de dados tem um modelo correspondente que especifica o tipo de dados. As seções a seguir discutem o formulário e as partes dos objetos de dados.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Dados (formato de arquivo X, codificação de texto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1af117a0207ce804ccacd397bb990fe5f43c94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370240"
---
# <a name="data-x-file-format-text-encoding"></a><span data-ttu-id="96fdf-105">Dados (formato de arquivo X, codificação de texto)</span><span class="sxs-lookup"><span data-stu-id="96fdf-105">Data (X file format, text encoding)</span></span>

<span data-ttu-id="96fdf-106">Os objetos de dados contêm os dados reais ou uma referência a esses dados.</span><span class="sxs-lookup"><span data-stu-id="96fdf-106">Data objects contain the actual data or a reference to that data.</span></span> <span data-ttu-id="96fdf-107">Cada objeto de dados tem um modelo correspondente que especifica o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="96fdf-107">Each data object has a corresponding template that specifies the data type.</span></span> <span data-ttu-id="96fdf-108">As seções a seguir discutem o formulário e as partes dos objetos de dados.</span><span class="sxs-lookup"><span data-stu-id="96fdf-108">The following sections discuss the form and parts of data objects.</span></span>

## <a name="form-identifier-and-name"></a><span data-ttu-id="96fdf-109">Formulário, identificador e nome</span><span class="sxs-lookup"><span data-stu-id="96fdf-109">Form, Identifier, and Name</span></span>

<span data-ttu-id="96fdf-110">Os objetos de dados têm o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="96fdf-110">Data objects have the following form.</span></span>


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



<span data-ttu-id="96fdf-111">O identificador é obrigatório e deve corresponder a um tipo de dados definido anteriormente ou primitivo.</span><span class="sxs-lookup"><span data-stu-id="96fdf-111">The identifier is compulsory and must match a previously defined data type or primitive.</span></span> <span data-ttu-id="96fdf-112">No entanto, o nome é opcional.</span><span class="sxs-lookup"><span data-stu-id="96fdf-112">However, the name is optional.</span></span>

## <a name="data-members"></a><span data-ttu-id="96fdf-113">Membros de dados</span><span class="sxs-lookup"><span data-stu-id="96fdf-113">Data Members</span></span>

<span data-ttu-id="96fdf-114">Os membros de dados podem ser um dos seguintes: objeto de dados, referência de dados, lista de inteiros, lista flutuante ou lista de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="96fdf-114">Data members can be one of the following: data object, data reference, integer list, float list, or string list.</span></span>

<span data-ttu-id="96fdf-115">Um objeto de dados é um objeto de dados aninhado.</span><span class="sxs-lookup"><span data-stu-id="96fdf-115">A data object is a nested data object.</span></span> <span data-ttu-id="96fdf-116">Isso permite que a natureza hierárquica do formato de arquivo seja expressa.</span><span class="sxs-lookup"><span data-stu-id="96fdf-116">This enables the hierarchical nature of the file format to be expressed.</span></span> <span data-ttu-id="96fdf-117">Os tipos de objetos de dados aninhados permitidos na hierarquia podem ser restritos.</span><span class="sxs-lookup"><span data-stu-id="96fdf-117">The types of nested data objects allowed in the hierarchy may be restricted.</span></span>

<span data-ttu-id="96fdf-118">Uma referência de dados é uma referência a um objeto de dados encontrado anteriormente, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="96fdf-118">A data reference is a reference to a previously encountered data object as shown in the following example.</span></span>


```
{
  name |
  UUID |
  name UUID
}
```



<span data-ttu-id="96fdf-119">Uma lista de inteiros é uma lista de inteiros separados por ponto e vírgula, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="96fdf-119">An integer list is a semicolon-separated list of integers, as shown in the following example.</span></span>


```
1; 2; 3;
```



<span data-ttu-id="96fdf-120">Uma lista flutuante é uma lista de floats separada por ponto e vírgula, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="96fdf-120">A float list is a semicolon-separated list of floats, as shown in the following example.</span></span>


```
1.0; 2.0; 3.0;
```



<span data-ttu-id="96fdf-121">Uma lista de cadeias de caracteres é uma lista separada por ponto-e-vírgula de cadeias, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="96fdf-121">A string list is a semicolon-separated list of strings, as shown in the following example.</span></span>


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a><span data-ttu-id="96fdf-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96fdf-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96fdf-123">Codificação de Texto</span><span class="sxs-lookup"><span data-stu-id="96fdf-123">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



