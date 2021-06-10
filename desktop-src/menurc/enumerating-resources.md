---
title: Enumerando recursos
description: Este tópico discute as funções usadas para obter listas de recursos.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: b978636303f3fc5bcae8c1d854289dde42ae0247
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910264"
---
# <a name="enumerating-resources"></a><span data-ttu-id="2f7b6-103">Enumerando recursos</span><span class="sxs-lookup"><span data-stu-id="2f7b6-103">Enumerating resources</span></span>

<span data-ttu-id="2f7b6-104">Em determinadas situações, talvez você queira descobrir o conteúdo do recurso de um módulo PE (executável portátil) desconhecido.</span><span class="sxs-lookup"><span data-stu-id="2f7b6-104">In certain situations, you might want to discover the resource contents of an unknown portable executable (PE) module.</span></span> <span data-ttu-id="2f7b6-105">O SDK do Windows fornece funções de enumeração de recursos que permitem que seu aplicativo obtenha listas de tipos de recursos, nomes e idiomas em um módulo especificado.</span><span class="sxs-lookup"><span data-stu-id="2f7b6-105">The Windows SDK provides resource enumeration functions that enable your application to obtain lists of resource types, names, and languages in a specified module.</span></span>

* <span data-ttu-id="2f7b6-106">As [**funções EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) [**e EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) fornecem uma lista de tipos de recursos encontrados no módulo.</span><span class="sxs-lookup"><span data-stu-id="2f7b6-106">The [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) and [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) functions provide a list of resource types found in the module.</span></span>
* <span data-ttu-id="2f7b6-107">As [**funções EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) [**e EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) fornecem o nome de cada recurso dentro de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="2f7b6-107">The [**EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) and [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) functions provide the name of each resource within a given type.</span></span>
* <span data-ttu-id="2f7b6-108">As [**funções EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) [**e EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) fornecem o idioma de cada recurso de um determinado nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="2f7b6-108">The [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) and [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) functions provide the language of each resource of a given name and type.</span></span> 

<span data-ttu-id="2f7b6-109">Essas funções e suas funções de retorno de chamada associadas permitem que seu aplicativo crie uma lista de todos os recursos em um módulo.</span><span class="sxs-lookup"><span data-stu-id="2f7b6-109">These functions and their associated callback functions enable your application to create a list of all resources in a module.</span></span> <span data-ttu-id="2f7b6-110">Esse processo é descrito em [Criando uma lista de recursos](using-resources.md).</span><span class="sxs-lookup"><span data-stu-id="2f7b6-110">This process is described in [Creating a resource list](using-resources.md).</span></span>

## <a name="-see-also"></a><span data-ttu-id="2f7b6-111">-see-also</span><span class="sxs-lookup"><span data-stu-id="2f7b6-111">-see-also</span></span>

[<span data-ttu-id="2f7b6-112">Msistuff.exe aplicativo de exemplo</span><span class="sxs-lookup"><span data-stu-id="2f7b6-112">Msistuff.exe sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
