---
description: O tipo de identificador do tipo semântico é um dos tipos de formato de texto.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Tipo de identificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091537"
---
# <a name="identifier-type"></a><span data-ttu-id="2316a-103">Tipo de identificador</span><span class="sxs-lookup"><span data-stu-id="2316a-103">Identifier Type</span></span>

<span data-ttu-id="2316a-104">O tipo de identificador do [tipo semântico](semantic-types.md) é um dos [tipos de formato de texto](text-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="2316a-104">The Identifier Type of [semantic type](semantic-types.md) is one of the [Text Format Types](text-format-types.md).</span></span> <span data-ttu-id="2316a-105">Esse tipo consiste em uma cadeia de caracteres de texto fornecida pelo usuário no formato de um [identificador](identifier.md)de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2316a-105">This type consists of an text string provided by the user in the format of a Windows Installer [Identifier](identifier.md).</span></span> <span data-ttu-id="2316a-106">A ferramenta de mesclagem substitui essa cadeia de caracteres nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="2316a-106">The merge tool substitutes this string into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="2316a-107">Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, inserir "0" na coluna formato, inserir "identificador" na coluna tipo e deixar em branco a coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md). A cadeia de caracteres pode estar em qualquer idioma compatível com a página de código do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2316a-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "0" into the Format column, enter "Identifier" into the Type column, and leave blank the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).The string may be in any language compatible with the code page of the database.</span></span> <span data-ttu-id="2316a-108">Consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="2316a-108">See [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span> <span data-ttu-id="2316a-109">NULL é um valor válido para a cadeia de caracteres de texto, a menos que o msmConfigItemNonNullable tenha sido incluído no campo atributos da Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2316a-109">Null is a valid value for the text string unless the msmConfigItemNonNullable has been included in the Attributes field of the ModuleConfiguration table.</span></span>

 

 



