---
description: O &\# 0034; O campo \# de bits&0034; tipo sem solicitações de contexto que o usuário fornece um inteiro cujo valor é usado para definir um ou mais bits em um campo de conteúdo. Esse texto pode estar em qualquer idioma compatível com a página de código do banco de dados.
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Tipo de campo de bits arbitrário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6571b8585c94577927df8cfedaded802a67d125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091544"
---
# <a name="arbitrary-bitfield-type"></a><span data-ttu-id="d339d-104">Tipo de campo de bits arbitrário</span><span class="sxs-lookup"><span data-stu-id="d339d-104">Arbitrary Bitfield Type</span></span>

<span data-ttu-id="d339d-105">O tipo "campo de teletexto" sem solicitações de contexto que o usuário fornece um inteiro cujo valor é usado para definir um ou mais bits em um teletipo.</span><span class="sxs-lookup"><span data-stu-id="d339d-105">The "Bitfield" type with no context requests that the user provide an integer whose value is used to set one or more bits in a bitfield.</span></span> <span data-ttu-id="d339d-106">Esse texto pode estar em qualquer idioma compatível com a página de código do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d339d-106">This text may be in any language compatible with the code page of the database.</span></span>

<span data-ttu-id="d339d-107">O tipo de linguagem de bits arbitrária do [tipo semântico](semantic-types.md) é um dos tipos de campo de bits.</span><span class="sxs-lookup"><span data-stu-id="d339d-107">The Arbitrary Bitfield Type of [semantic type](semantic-types.md) is one of the Bitfield Types.</span></span> <span data-ttu-id="d339d-108">Esse tipo consiste em um inteiro escolhido pelo usuário de um conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="d339d-108">This type consists of an integer chosen by the user from a set of choices.</span></span> <span data-ttu-id="d339d-109">A ferramenta de mesclagem substitui o inteiro selecionado nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="d339d-109">The merge tool substitutes the selected integer into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="d339d-110">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item na coluna nome, inserir "3" na coluna formato, deixar a coluna tipo em branco e inserir a lista de inteiros possíveis na coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="d339d-110">To specify a configurable item of this type, module authors should enter the name of the item into the Name column, enter "3" into the Format column, leave the Type column blank, and enter the list of possible integers in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="d339d-111">A coluna de tipo é reservada e deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="d339d-111">The Type column is reserved and must be null.</span></span> <span data-ttu-id="d339d-112">A entrada na coluna ContextData para todos os tipos de formato de campo de bits deve estar no formato " <mask> ;<Name>=</span><span class="sxs-lookup"><span data-stu-id="d339d-112">The entry in the ContextData column for all Bitfield Format types must be in the form "<mask>;<Name>=</span></span><value><span data-ttu-id="d339d-113">;<Name>=</span><span class="sxs-lookup"><span data-stu-id="d339d-113">;<Name>=</span></span><value><span data-ttu-id="d339d-114">.... ", em que <mask> é um valor inteiro que indica os bits de interesse, <Name> é um nome de exibição localizável para a escolha e</span><span class="sxs-lookup"><span data-stu-id="d339d-114">....", where <mask> is an integer value indicating the bits of interest, <Name> is a localizable display name for the choice, and</span></span> <value> <span data-ttu-id="d339d-115">é um valor inteiro decimal.</span><span class="sxs-lookup"><span data-stu-id="d339d-115">is a decimal integer value.</span></span> <span data-ttu-id="d339d-116">A coluna de contexto está em usar o [formato especial CMSM](cmsm-special-format.md) e para todos os tipos de campo de bits.</span><span class="sxs-lookup"><span data-stu-id="d339d-116">The context column is in use [CMSM Special Format](cmsm-special-format.md) and for all bitfield types.</span></span> <span data-ttu-id="d339d-117">Um caractere literal "=" ou ";" pode ser inserido no <Name> campo prefixando-o com um caractere de barra invertida (' \\ ').</span><span class="sxs-lookup"><span data-stu-id="d339d-117">A literal "=" or ";" character can be entered in the <Name> field by prefixing it with a backslash ('\\') character.</span></span>

 

 



