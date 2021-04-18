---
description: O tipo de tipo de semântica RTF é um dos tipos de formato de texto.
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: Tipo RTF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81c708183596d794f20e38bf89c073472e3affb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750220"
---
# <a name="rtf-type"></a><span data-ttu-id="84995-103">Tipo RTF</span><span class="sxs-lookup"><span data-stu-id="84995-103">RTF Type</span></span>

<span data-ttu-id="84995-104">O tipo de [tipo de semântica](semantic-types.md) RTF é um dos [tipos de formato de texto](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="84995-104">The RTF Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="84995-105">Esse tipo consiste em uma cadeia de caracteres de texto arbitrária no RTF (Rich Text Format) de qualquer comprimento fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="84995-105">This type consists of an arbitrary text string in the Rich Text Format (RTF) of any length provided by the user.</span></span> <span data-ttu-id="84995-106">A ferramenta de mesclagem substitui essa cadeia de caracteres nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="84995-106">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="84995-107">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, inserir "0" na coluna formato, inserir "RTF" na coluna tipo e deixar em branco a coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md). A cadeia de caracteres pode estar em qualquer idioma compatível com a página de código do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="84995-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "RTF" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="84995-108">Consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="84995-108">See [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="84995-109">NULL é um valor válido para a cadeia de caracteres de texto, a menos que o msmConfigItemNonNullable tenha sido incluído no campo atributos da Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="84995-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



