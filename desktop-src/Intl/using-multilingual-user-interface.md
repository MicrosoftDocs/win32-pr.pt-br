---
description: Usando a interface do usuário multilíngue
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: Usando a interface do usuário multilíngue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287acc88d144c7775d2125cbb4a055784370d87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172176"
---
# <a name="using-multilingual-user-interface"></a><span data-ttu-id="be1b5-103">Usando a interface do usuário multilíngue</span><span class="sxs-lookup"><span data-stu-id="be1b5-103">Using Multilingual User Interface</span></span>

<span data-ttu-id="be1b5-104">Esta seção descreve como usar a funcionalidade MUI (Multilingual User interface) para projetar e implementar seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="be1b5-104">This section describes how to use Multilingual User Interface (MUI) functionality to design and implement your applications.</span></span> <span data-ttu-id="be1b5-105">Veja a seguir os aspectos da tecnologia MUI que entrarão em cena na maioria dos estágios do ciclo de vida do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="be1b5-105">The following are aspects of MUI technology that will come into play at most stages of the application lifecycle.</span></span>

-   <span data-ttu-id="be1b5-106">Desenvolvimento de aplicativos, incluindo preparação de recursos, configuração de preferências de idioma do aplicativo, localização e carregamento de recursos</span><span class="sxs-lookup"><span data-stu-id="be1b5-106">Application development, including resource preparation, setting of application language preferences, finding and loading of resources</span></span>
-   <span data-ttu-id="be1b5-107">Compilando e localizando o aplicativo</span><span class="sxs-lookup"><span data-stu-id="be1b5-107">Building and localizing the application</span></span>
-   <span data-ttu-id="be1b5-108">Implantação do aplicativo</span><span class="sxs-lookup"><span data-stu-id="be1b5-108">Deploying the application</span></span>

<span data-ttu-id="be1b5-109">Aqui estão algumas perguntas a serem consideradas ao projetar e implementar um aplicativo MUI.</span><span class="sxs-lookup"><span data-stu-id="be1b5-109">Here are some questions to consider when designing and implementing a MUI application.</span></span>

-   <span data-ttu-id="be1b5-110">Quais são as versões do Windows para as quais o aplicativo dará suporte?</span><span class="sxs-lookup"><span data-stu-id="be1b5-110">What are the versions of Windows that the application will support?</span></span>
-   <span data-ttu-id="be1b5-111">Em quais idiomas o aplicativo será localizado?</span><span class="sxs-lookup"><span data-stu-id="be1b5-111">In what languages will the application be localized?</span></span>
-   <span data-ttu-id="be1b5-112">As configurações de idioma do aplicativo devem sempre seguir as configurações de idioma do sistema operacional ou o usuário do aplicativo poderá definir idiomas específicos?</span><span class="sxs-lookup"><span data-stu-id="be1b5-112">Should the application language settings always follow language settings for the operating system, or should the application user be able to set specific languages?</span></span>
-   <span data-ttu-id="be1b5-113">Que tipo de recursos de interface do usuário o aplicativo usa e onde eles são armazenados?</span><span class="sxs-lookup"><span data-stu-id="be1b5-113">What type of user interface resources does the application use and where are they stored?</span></span>

<span data-ttu-id="be1b5-114">Esta seção inclui os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="be1b5-114">This section includes the following topics.</span></span> <span data-ttu-id="be1b5-115">As descrições pressupõem um aplicativo MUI direcionado ao Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="be1b5-115">The descriptions assume a MUI application targeted at Windows Vista and later.</span></span> <span data-ttu-id="be1b5-116">Os recursos para esse aplicativo são recursos do Win32, com recursos específicos de idioma e código executável que residem em arquivos do Win32 PE separados.</span><span class="sxs-lookup"><span data-stu-id="be1b5-116">The resources for this application are Win32 resources, with language-specific resources and executable code residing in separate Win32 PE files.</span></span> <span data-ttu-id="be1b5-117">Considerações especiais para o suporte de sistemas operacionais anteriores ao Windows Vista ou para diferentes tipos de recursos são adicionadas conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="be1b5-117">Special considerations for support of pre-Windows Vista operating systems or for different types of resources are added as appropriate.</span></span>

-   [<span data-ttu-id="be1b5-118">Preparando recursos</span><span class="sxs-lookup"><span data-stu-id="be1b5-118">Preparing Resources</span></span>](preparing-resources.md)
-   [<span data-ttu-id="be1b5-119">Definindo preferências de idioma do aplicativo</span><span class="sxs-lookup"><span data-stu-id="be1b5-119">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
-   [<span data-ttu-id="be1b5-120">Localizando recursos do Win32 PE</span><span class="sxs-lookup"><span data-stu-id="be1b5-120">Locating Win32 PE Resources</span></span>](locating-win32-pe-resources.md)
-   [<span data-ttu-id="be1b5-121">Localizando recursos não Win32 PE</span><span class="sxs-lookup"><span data-stu-id="be1b5-121">Locating Non-Win32 PE Resources</span></span>](locating-non-win32-pe-resources.md)
-   [<span data-ttu-id="be1b5-122">Localizando recursos e compilando o aplicativo</span><span class="sxs-lookup"><span data-stu-id="be1b5-122">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
-   [<span data-ttu-id="be1b5-123">MUI: exemplo de aplicativo de configurações do sistema</span><span class="sxs-lookup"><span data-stu-id="be1b5-123">MUI: System Settings Application Sample</span></span>](mui-system-settings-application-sample.md)
-   [<span data-ttu-id="be1b5-124">MUI: exemplo de configurações de Application-Specific (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="be1b5-124">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
-   [<span data-ttu-id="be1b5-125">MUI: exemplo de configurações de Application-Specific (pré-Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="be1b5-125">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)

 

 



