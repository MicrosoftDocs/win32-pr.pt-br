---
description: O tipo formatado de tipo semântico é um dos tipos de formato de texto.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Tipo formatado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b97e0c0c1763352f75424bf54d01f6871604f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010706"
---
# <a name="formatted-type"></a><span data-ttu-id="7abf0-103">Tipo formatado</span><span class="sxs-lookup"><span data-stu-id="7abf0-103">Formatted Type</span></span>

<span data-ttu-id="7abf0-104">O tipo formatado de [tipo semântico](semantic-types.md) é um dos [tipos de formato de texto](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="7abf0-104">The Formatted Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="7abf0-105">Esse tipo consiste em uma cadeia de caracteres de texto arbitrária de qualquer comprimento fornecido pelo usuário e no Windows Installer formato de texto formatado.</span><span class="sxs-lookup"><span data-stu-id="7abf0-105">This type consists of an arbitrary text string of any length provided by the user and in the Windows Installer formatted text format.</span></span> <span data-ttu-id="7abf0-106">Para obter detalhes, consulte [formatado](formatted.md).</span><span class="sxs-lookup"><span data-stu-id="7abf0-106">For details, see [Formatted](formatted.md).</span></span> <span data-ttu-id="7abf0-107">A ferramenta de mesclagem substitui essa cadeia de caracteres nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7abf0-107">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="7abf0-108">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, inserir "0" na coluna formato, inserir "formatado" na coluna tipo e deixar em branco a coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md). A cadeia de caracteres pode estar em qualquer idioma compatível com a página de código do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7abf0-108">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Formatted" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="7abf0-109">Para obter detalhes, consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="7abf0-109">For details, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="7abf0-110">NULL é um valor válido para a cadeia de caracteres de texto, a menos que o msmConfigItemNonNullable tenha sido incluído no campo atributos da Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7abf0-110">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



