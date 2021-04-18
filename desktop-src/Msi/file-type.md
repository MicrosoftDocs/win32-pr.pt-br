---
description: O tipo de arquivo do tipo semântico é um dos tipos de formato de chave. Esse tipo consiste em uma chave estrangeira na tabela de arquivos fornecida pelo usuário.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753269"
---
# <a name="file-type"></a><span data-ttu-id="23510-104">Tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="23510-104">File Type</span></span>

<span data-ttu-id="23510-105">O tipo de arquivo do [tipo semântico](semantic-types.md) é um dos [tipos de formato de chave](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="23510-105">The File Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="23510-106">Esse tipo consiste em uma chave estrangeira na [tabela de arquivos](file-table.md) fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="23510-106">This type consists of a foreign key into the [File table](file-table.md) provided by the user.</span></span>

<span data-ttu-id="23510-107">O tipo de arquivo pode ser usado com os seguintes tipos de ContextData.</span><span class="sxs-lookup"><span data-stu-id="23510-107">The File type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="23510-108">**AssemblyContext ContextData**</span><span class="sxs-lookup"><span data-stu-id="23510-108">**AssemblyContext ContextData**</span></span>

<span data-ttu-id="23510-109">Esse tipo pode ser usado para permitir que os usuários configurem chaves estrangeiras para assemblies Win32 ou Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="23510-109">This type may be used to enable users to configure foreign keys to Win32 or common language runtime assemblies.</span></span> <span data-ttu-id="23510-110">A ferramenta de mesclagem deve substituir um [identificador](identifier.md) de Windows Installer por itens desse tipo no modelo na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="23510-110">The merge tool must substitute a Windows Installer [Identifier](identifier.md) for items of this type into the template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="23510-111">Mergemod.dll não impõe isso e cabe à ferramenta de mesclagem garantir que o usuário forneça uma chave válida para a tabela de arquivos.</span><span class="sxs-lookup"><span data-stu-id="23510-111">Mergemod.dll does not enforce this and it is up to the merge tool to ensure that the user provides a valid key into the File table.</span></span>

<span data-ttu-id="23510-112">NULL é um valor válido para esse tipo, a menos que o msmConfigItemNonNullable tenha sido incluído no campo Attributes da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="23510-112">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



