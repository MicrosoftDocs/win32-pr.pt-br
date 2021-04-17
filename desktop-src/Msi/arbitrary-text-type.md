---
description: O tipo de texto arbitrário do tipo semântico é um dos tipos de formato de texto.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Tipo de texto arbitrário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750823"
---
# <a name="arbitrary-text-type"></a><span data-ttu-id="7a7ff-103">Tipo de texto arbitrário</span><span class="sxs-lookup"><span data-stu-id="7a7ff-103">Arbitrary Text Type</span></span>

<span data-ttu-id="7a7ff-104">O tipo de texto arbitrário do [tipo semântico](semantic-types.md) é um dos [tipos de formato de texto](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="7a7ff-104">The Arbitrary Text Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="7a7ff-105">Esse tipo consiste em uma cadeia de caracteres de texto arbitrária de qualquer comprimento fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7a7ff-105">This type consists of an arbitrary text string of any length provided by the user.</span></span> <span data-ttu-id="7a7ff-106">A ferramenta de mesclagem substitui essa cadeia de caracteres arbitrária nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a7ff-106">The merge tool substitutes this arbitrary string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="7a7ff-107">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, inserir "0" na coluna de formato e deixar em branco as colunas Type e ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md). A cadeia de caracteres de texto arbitrário pode estar em qualquer idioma compatível com a página de código do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7a7ff-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, and leave blank the Type and ContextData columns of the [ModuleConfiguration table](moduleconfiguration-table.md).The arbitrary text string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="7a7ff-108">Para obter detalhes, consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="7a7ff-108">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="7a7ff-109">NULL é um valor válido para a cadeia de caracteres de texto, a menos que o msmConfigItemNonNullable tenha sido incluído no campo atributos da Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7a7ff-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



