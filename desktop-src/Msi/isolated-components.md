---
description: Os autores de pacotes de instalação podem especificar que o instalador Copie os arquivos compartilhados (normalmente DLLs compartilhadas) de um aplicativo para a pasta desse aplicativo em vez de um local compartilhado.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Componentes isolados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f29f614dfd819e093c5729a9a97a076247d281d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646804"
---
# <a name="isolated-components"></a><span data-ttu-id="e759f-103">Componentes isolados</span><span class="sxs-lookup"><span data-stu-id="e759f-103">Isolated Components</span></span>

<span data-ttu-id="e759f-104">Os autores de pacotes de instalação podem especificar que o instalador Copie os arquivos compartilhados (normalmente DLLs compartilhadas) de um aplicativo para a pasta desse aplicativo em vez de um local compartilhado.</span><span class="sxs-lookup"><span data-stu-id="e759f-104">Authors of installation packages can specify that the installer copy the shared files (commonly shared DLLs) of an application into that application's folder rather than to a shared location.</span></span> <span data-ttu-id="e759f-105">Esse conjunto particular de arquivos (DLLs) é usado somente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e759f-105">This private set of files (DLLs) are then used only by the application.</span></span> <span data-ttu-id="e759f-106">Isolar o aplicativo junto com seus componentes compartilhados dessa maneira tem as seguintes vantagens:</span><span class="sxs-lookup"><span data-stu-id="e759f-106">Isolating the application together with its shared components in this manner has the following advantages:</span></span>

-   <span data-ttu-id="e759f-107">O aplicativo sempre usa as versões dos arquivos compartilhados com as quais ele foi implantado.</span><span class="sxs-lookup"><span data-stu-id="e759f-107">The application always uses the versions of the shared files with which it was deployed.</span></span>
-   <span data-ttu-id="e759f-108">A instalação do aplicativo não substitui outras versões dos arquivos compartilhados por outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e759f-108">Installing the application does not overwrite other versions of the shared files by other applications.</span></span>
-   <span data-ttu-id="e759f-109">As instalações subsequentes de outros aplicativos que usam versões diferentes dos arquivos compartilhados não podem substituir os arquivos usados por esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e759f-109">Subsequent installations of other applications using different versions of the shared files cannot overwrite the files used by this application.</span></span>

<span data-ttu-id="e759f-110">Como a implementação atual do COM mantém um único caminho completo no registro para cada par de CLSID/contexto, ele força todos os aplicativos a usarem a mesma versão de uma DLL compartilhada.</span><span class="sxs-lookup"><span data-stu-id="e759f-110">Because the current implementation of COM keeps a single full path in the registry for each CLSID/Context pair, it forces all applications to use the same version of a shared DLL.</span></span> <span data-ttu-id="e759f-111">Para permitir que um aplicativo mantenha uma cópia privada de um servidor COM, o carregador do sistema no Windows 2000 verifica a presença de um. Arquivo LOCAL na pasta do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e759f-111">To enable an application to keep a private copy of a COM server, the system loader in Windows 2000 checks for the presence of a .LOCAL file in the application's folder.</span></span> <span data-ttu-id="e759f-112">Se o carregador do sistema detectar um. Arquivo LOCAL, ele altera sua lógica de pesquisa para preferir DLLs localizadas na mesma pasta que o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e759f-112">If the system loader detects a .LOCAL file, it alters its search logic to prefer DLLs located in the same folder as the application.</span></span>

<span data-ttu-id="e759f-113">Quando Windows Installer executa a [ação IsolateComponents](isolatecomponents-action.md) , eles copiam os arquivos do componente (normalmente uma DLL compartilhada) especificada na \_ coluna compartilhada do componente da [tabela IsolatedComponent](isolatedcomponent-table.md) na mesma pasta que o componente (normalmente um arquivo. exe) especificado na \_ coluna aplicativo do componente.</span><span class="sxs-lookup"><span data-stu-id="e759f-113">When Windows Installer runs the [IsolateComponents action](isolatecomponents-action.md) they copy the files of the component (commonly a shared DLL) specified in the Component\_Shared column of the [IsolatedComponent table](isolatedcomponent-table.md) into the same folder as the component (commonly an .exe file) specified in the Component\_Application column.</span></span> <span data-ttu-id="e759f-114">O instalador cria um arquivo nesse diretório, com comprimento de zero bytes, tendo o nome de arquivo curto do arquivo de chave para o aplicativo de componente \_ (normalmente, o nome é o mesmo que o. exe do aplicativo) acrescentado com. LOCAL.</span><span class="sxs-lookup"><span data-stu-id="e759f-114">The installer creates a file in this directory, zero bytes in length, having the short file name of the key file for Component\_Application (typically the name is the same as the application's .exe) appended with .LOCAL.</span></span> <span data-ttu-id="e759f-115">O instalador usa o registro para o componente em seu local compartilhado e não grava nenhuma informação de registro para a cópia do componente no local privado.</span><span class="sxs-lookup"><span data-stu-id="e759f-115">The installer uses the registration for the component in its shared location and does not write any registration information for the copy of the component in the private location.</span></span>

<span data-ttu-id="e759f-116">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="e759f-116">For more information, see:</span></span>

-   [<span data-ttu-id="e759f-117">Instalação de componentes isolados</span><span class="sxs-lookup"><span data-stu-id="e759f-117">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
-   [<span data-ttu-id="e759f-118">Reinstalação de componentes isolados</span><span class="sxs-lookup"><span data-stu-id="e759f-118">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
-   [<span data-ttu-id="e759f-119">Remoção de componentes isolados</span><span class="sxs-lookup"><span data-stu-id="e759f-119">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
-   [<span data-ttu-id="e759f-120">Usando componentes isolados</span><span class="sxs-lookup"><span data-stu-id="e759f-120">Using Isolated Components</span></span>](using-isolated-components.md)

 

 



