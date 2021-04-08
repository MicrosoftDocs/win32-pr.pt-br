---
description: O tipo de enumeração do tipo semântico é um dos tipos de formato de texto.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Tipo de enumeração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc582a7f96d8fc91aad66387f579f05f9255346f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921374"
---
# <a name="enum-type"></a><span data-ttu-id="f3d39-103">Tipo de enumeração</span><span class="sxs-lookup"><span data-stu-id="f3d39-103">Enum Type</span></span>

<span data-ttu-id="f3d39-104">O tipo de enumeração do [tipo semântico](semantic-types.md) é um dos [tipos de formato de texto](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="f3d39-104">The Enum Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="f3d39-105">Esse tipo consiste em uma cadeia de caracteres de texto escolhida pelo usuário a partir de um conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="f3d39-105">This type consists of a text string chosen by the user from a set of choices.</span></span> <span data-ttu-id="f3d39-106">A ferramenta de mesclagem substitui a cadeia de caracteres selecionada selecionada nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="f3d39-106">The merge tool substitutes the selected string selected into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="f3d39-107">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, digitar "0" na coluna formato, digitar "enum" na coluna tipo e inserir a lista de possíveis cadeias de caracteres na coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="f3d39-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Enum" into the Type column, and enter the list of possible strings in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="f3d39-108">A lista de cadeias de caracteres possíveis deve ser fornecida como uma lista de cadeias de caracteres deliminated por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="f3d39-108">The list of possible strings must be provided as a list of strings deliminated by semicolons.</span></span> <span data-ttu-id="f3d39-109">Cada opção deve estar no formato "nome = valor".</span><span class="sxs-lookup"><span data-stu-id="f3d39-109">Each choice must be in the form "Name=Value".</span></span> <span data-ttu-id="f3d39-110">Um ponto-e-vírgula literal pode ser adicionado ao valor prefixando o ponto e vírgula com um caractere de barra invertida.</span><span class="sxs-lookup"><span data-stu-id="f3d39-110">A literal semicolon can be added to the value by prefixing the semicolon with a backslash character.</span></span> <span data-ttu-id="f3d39-111">NULL é um valor válido, a menos que msmConfigItemNonNullable tenha sido incluído no campo Attributes da Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f3d39-111">Null is a valid value unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



