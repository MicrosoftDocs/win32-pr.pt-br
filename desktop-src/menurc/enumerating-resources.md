---
title: Enumerando recursos
description: Este tópico discute as funções usadas para obter listas de recursos.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ea7f2600f6da98cff6f16853092004a542b0f206
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105751995"
---
# <a name="enumerating-resources"></a><span data-ttu-id="1071a-103">Enumerando recursos</span><span class="sxs-lookup"><span data-stu-id="1071a-103">Enumerating resources</span></span>

<span data-ttu-id="1071a-104">Em determinadas situações, talvez você queira descobrir o conteúdo do recurso de um módulo executável portátil (PE) desconhecido.</span><span class="sxs-lookup"><span data-stu-id="1071a-104">In certain situations, you might want to discover the resource contents of an unknown portable executable (PE) module.</span></span> <span data-ttu-id="1071a-105">O SDK do Windows fornece funções de enumeração de recursos que permitem que seu aplicativo obtenha listas de tipos de recursos, nomes e idiomas em um módulo especificado.</span><span class="sxs-lookup"><span data-stu-id="1071a-105">The Windows SDK provides resource enumeration functions that enable your application to obtain lists of resource types, names, and languages in a specified module.</span></span>

* <span data-ttu-id="1071a-106">As funções [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) e [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) fornecem uma lista de tipos de recursos encontrados no módulo.</span><span class="sxs-lookup"><span data-stu-id="1071a-106">The [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) and [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) functions provide a list of resource types found in the module.</span></span>
* <span data-ttu-id="1071a-107">As funções [**EnumResourceNamesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcenamesw) e [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) fornecem o nome de cada recurso dentro de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="1071a-107">The [**EnumResourceNamesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcenamesw) and [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) functions provide the name of each resource within a given type.</span></span>
* <span data-ttu-id="1071a-108">As funções [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) e [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) fornecem o idioma de cada recurso de um determinado nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="1071a-108">The [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) and [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) functions provide the language of each resource of a given name and type.</span></span> 

<span data-ttu-id="1071a-109">Essas funções e suas funções de retorno de chamada associadas permitem que seu aplicativo crie uma lista de todos os recursos em um módulo.</span><span class="sxs-lookup"><span data-stu-id="1071a-109">These functions and their associated callback functions enable your application to create a list of all resources in a module.</span></span> <span data-ttu-id="1071a-110">Esse processo é descrito em [criando uma lista de recursos](using-resources.md).</span><span class="sxs-lookup"><span data-stu-id="1071a-110">This process is described in [Creating a resource list](using-resources.md).</span></span>

## <a name="-see-also"></a><span data-ttu-id="1071a-111">-Consulte-também</span><span class="sxs-lookup"><span data-stu-id="1071a-111">-see-also</span></span>

[<span data-ttu-id="1071a-112">Msistuff.exe aplicativo de exemplo</span><span class="sxs-lookup"><span data-stu-id="1071a-112">Msistuff.exe sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
