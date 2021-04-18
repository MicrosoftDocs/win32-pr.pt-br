---
description: O Windows Installer pode anunciar a disponibilidade de um aplicativo para usuários ou outros aplicativos sem realmente instalar o aplicativo.
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: Anúncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bb31f14fb4cd6f589e94939afdd5575df52c43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749596"
---
# <a name="advertisement"></a><span data-ttu-id="4348e-103">Anúncio</span><span class="sxs-lookup"><span data-stu-id="4348e-103">Advertisement</span></span>

<span data-ttu-id="4348e-104">O Windows Installer pode anunciar a disponibilidade de um aplicativo para usuários ou outros aplicativos sem realmente instalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4348e-104">The Windows Installer can advertise the availability of an application to users or other applications without actually installing the application.</span></span> <span data-ttu-id="4348e-105">Se um aplicativo for anunciado, somente as interfaces necessárias para carregar e iniciar o aplicativo serão apresentadas ao usuário ou a outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4348e-105">If an application is advertised, only the interfaces required for loading and launching the application are presented to the user or other applications.</span></span> <span data-ttu-id="4348e-106">Se um usuário ou aplicativo ativar uma interface anunciada, o instalador continuará instalando os componentes necessários, conforme descrito em [instalação sob demanda](installation-on-demand.md).</span><span class="sxs-lookup"><span data-stu-id="4348e-106">If a user or application activates an advertised interface the installer then proceeds to install the necessary components as described in [Installation-On-Demand](installation-on-demand.md).</span></span>

<span data-ttu-id="4348e-107">Os dois tipos de publicidade são atribuição e publicação.</span><span class="sxs-lookup"><span data-stu-id="4348e-107">The two types of advertising are assigning and publishing.</span></span> <span data-ttu-id="4348e-108">Um aplicativo aparece instalado para um usuário quando esse aplicativo é atribuído ao usuário.</span><span class="sxs-lookup"><span data-stu-id="4348e-108">An application appears installed to a user when that application is assigned to the user.</span></span> <span data-ttu-id="4348e-109">O menu **Iniciar** contém os atalhos apropriados, os ícones são exibidos, os arquivos são associados ao aplicativo e as entradas do registro refletem a instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4348e-109">The **Start** menu contains the appropriate shortcuts, icons are displayed, files are associated with the application, and registry entries reflect the application's installation.</span></span> <span data-ttu-id="4348e-110">Quando o usuário tenta abrir um aplicativo atribuído, ele é instalado sob demanda.</span><span class="sxs-lookup"><span data-stu-id="4348e-110">When the user tries to open an assigned application it is installed upon demand.</span></span>

<span data-ttu-id="4348e-111">O instalador oferece suporte ao anúncio de aplicativos e recursos de acordo com o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4348e-111">The installer supports the advertisement of applications and features according to the operating system.</span></span> <span data-ttu-id="4348e-112">O instalador registra informações de classe COM para aplicativos atribuídos a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4348e-112">The installer registers COM class information for assigned applications beginning with Windows XP.</span></span> <span data-ttu-id="4348e-113">Isso permite que o instalador instale o aplicativo na criação de uma instância de uma classe anunciada.</span><span class="sxs-lookup"><span data-stu-id="4348e-113">This enables the installer to install the application upon the creation of an instance of an advertised class.</span></span> <span data-ttu-id="4348e-114">Para obter mais informações, consulte [suporte de plataforma do anúncio](platform-support-of-advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="4348e-114">For more information, see [Platform Support of Advertisement](platform-support-of-advertisement.md).</span></span>

<span data-ttu-id="4348e-115">Você pode publicar um aplicativo do servidor a partir do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4348e-115">You can publish an application from the server beginning with Windows Server 2003.</span></span> <span data-ttu-id="4348e-116">O aplicativo publicado é instalado por meio de sua associação de arquivo ou do tipo MIME (Multipurpose Internet Mail Extension).</span><span class="sxs-lookup"><span data-stu-id="4348e-116">The published application is then installed through its file association or Multipurpose Internet Mail Extension (MIME) type.</span></span> <span data-ttu-id="4348e-117">A publicação não preenche a interface do usuário com nenhum dos ícones do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4348e-117">Publishing does not populate the user interface with any of the application's icons.</span></span> <span data-ttu-id="4348e-118">O sistema operacional do cliente pode instalar um aplicativo publicado a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4348e-118">The client operating system can install a published application beginning with Windows XP.</span></span>

 

 



