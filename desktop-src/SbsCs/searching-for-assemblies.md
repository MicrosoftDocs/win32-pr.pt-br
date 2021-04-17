---
description: Há dois métodos pelos quais um aplicativo de hospedagem pode pesquisar assemblies lado a lado.
ms.assetid: f34f8f39-f03c-4adf-afa8-9cb9ed48d149
title: Pesquisando assemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f257b7da8099508fb268623a175d8ebd8e9d8337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747856"
---
# <a name="searching-for-assemblies"></a><span data-ttu-id="1fd5c-103">Pesquisando assemblies</span><span class="sxs-lookup"><span data-stu-id="1fd5c-103">Searching for Assemblies</span></span>

<span data-ttu-id="1fd5c-104">Há dois métodos pelos quais um aplicativo de hospedagem pode pesquisar assemblies lado a lado.</span><span class="sxs-lookup"><span data-stu-id="1fd5c-104">There are two methods by which a hosting application can search for side-by-side assemblies.</span></span>

<span data-ttu-id="1fd5c-105">Os módulos hospedados podem se registrar com o aplicativo de hospedagem, estendendo algumas informações de configuração compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="1fd5c-105">Hosted modules can register themselves with the hosting application by extending some shared configuration information.</span></span> <span data-ttu-id="1fd5c-106">O aplicativo pode usar essas informações de configuração para carregar os assemblies necessários para a nova funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="1fd5c-106">The application can then use this configuration information to load the assemblies required for the new functionality.</span></span> <span data-ttu-id="1fd5c-107">Isso pode ser feito chamando [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) em manifestos especificados nos dados de registro, seguido chamando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para entrar no novo módulo.</span><span class="sxs-lookup"><span data-stu-id="1fd5c-107">This could be done by calling [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) on manifests specified in the registration data, followed by calling [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get into the new module.</span></span> <span data-ttu-id="1fd5c-108">Observe que, com esse método, os novos componentes precisam atualizar algum estado do aplicativo compartilhado para indicar sua presença.</span><span class="sxs-lookup"><span data-stu-id="1fd5c-108">Note that with this method, the new components have to update some shared application state to indicate their presence.</span></span>

<span data-ttu-id="1fd5c-109">O aplicativo de hospedagem pode pesquisar ativamente os assemblies na inicialização usando o [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) e o [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) para procurar DLLs ou manifestos em um local especificado e, em seguida, usar [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) para acessar as informações.</span><span class="sxs-lookup"><span data-stu-id="1fd5c-109">The hosting application can actively search for the assemblies on startup using [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) to look for DLLs or manifests in a specified location, and then use [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) to access the information.</span></span> <span data-ttu-id="1fd5c-110">Esse método não requer nenhum registro do componente.</span><span class="sxs-lookup"><span data-stu-id="1fd5c-110">This method requires no registration of the component.</span></span>

 

 
