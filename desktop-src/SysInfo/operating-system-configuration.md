---
description: O diretório do Windows é o diretório que contém aplicativos baseados no Windows, arquivos de inicialização e arquivos de ajuda. A função GetWindowsDirectory recupera o caminho para esse diretório.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Configuração do sistema operacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38aa2c2b6b4f6b3ac5caac78a89ad980a9bd074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170634"
---
# <a name="operating-system-configuration"></a><span data-ttu-id="46815-104">Configuração do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="46815-104">Operating System Configuration</span></span>

<span data-ttu-id="46815-105">O *diretório do Windows* é o diretório que contém aplicativos baseados no Windows, arquivos de inicialização e arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="46815-105">The *Windows directory* is the directory that contains Windows-based applications, initialization files, and help files.</span></span> <span data-ttu-id="46815-106">A função [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) recupera o caminho para esse diretório.</span><span class="sxs-lookup"><span data-stu-id="46815-106">The [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="46815-107">O *diretório do sistema* é o diretório que contém bibliotecas de vínculo dinâmico, drivers e arquivos de fonte.</span><span class="sxs-lookup"><span data-stu-id="46815-107">The *system directory* is the directory that contains dynamic-link libraries, drivers, and font files.</span></span> <span data-ttu-id="46815-108">A função [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) recupera o caminho para esse diretório.</span><span class="sxs-lookup"><span data-stu-id="46815-108">The [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="46815-109">A função [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) recupera o nome do usuário atualmente conectado ao sistema.</span><span class="sxs-lookup"><span data-stu-id="46815-109">The [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) function retrieves the name of the user currently logged onto the system.</span></span> <span data-ttu-id="46815-110">O nome de usuário será o nome de logon ou o nome completo do usuário, se o último estiver incluído no registro.</span><span class="sxs-lookup"><span data-stu-id="46815-110">The user name is either the logon name or the user's full name, if the latter is included in the registry.</span></span>

<span data-ttu-id="46815-111">Uma *variável de ambiente* é uma variável simbólica que representa algum elemento do sistema, como um caminho, um nome de arquivo ou outros dados literais.</span><span class="sxs-lookup"><span data-stu-id="46815-111">An *environment variable* is a symbolic variable that represents some element of the system, such as a path, a file name, or other literal data.</span></span> <span data-ttu-id="46815-112">Por exemplo, o caminho da variável de ambiente representa os diretórios nos quais pesquisar arquivos executáveis.</span><span class="sxs-lookup"><span data-stu-id="46815-112">For example, the environment variable PATH represents the directories in which to search for executable files.</span></span> <span data-ttu-id="46815-113">Quando um usuário faz logon, o sistema inicializa as variáveis de ambiente com base na seção ambiente do registro.</span><span class="sxs-lookup"><span data-stu-id="46815-113">When a user logs on, the system initializes environment variables based on the environment section of the registry.</span></span> <span data-ttu-id="46815-114">A função [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) recupera os valores das variáveis de ambiente especificadas.</span><span class="sxs-lookup"><span data-stu-id="46815-114">The [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) function retrieves the values of specified environment variables.</span></span>

<span data-ttu-id="46815-115">Informações adicionais são fornecidas pela interface [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) .</span><span class="sxs-lookup"><span data-stu-id="46815-115">Additional information is provided by the [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) interface.</span></span>

 

 
