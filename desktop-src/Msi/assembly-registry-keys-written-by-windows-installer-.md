---
description: Se um pacote de Windows Installer instalar ou anunciar assemblies, o instalador armazenará informações sobre esses assemblies no registro do sistema local.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Chaves do registro de assembly gravadas por Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505799"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a><span data-ttu-id="43589-103">Chaves do registro de assembly gravadas por Windows Installer</span><span class="sxs-lookup"><span data-stu-id="43589-103">Assembly Registry Keys Written by Windows Installer</span></span>

<span data-ttu-id="43589-104">Se um pacote de Windows Installer instalar ou anunciar assemblies, o instalador armazenará informações sobre esses assemblies no registro do sistema local.</span><span class="sxs-lookup"><span data-stu-id="43589-104">If a Windows Installer package installs or advertises assemblies, the installer stores information about those assemblies in the local system registry.</span></span> <span data-ttu-id="43589-105">Observe que essas chaves do registro são destinadas apenas para serem usadas internamente pelo Windows Installer e não devem ser contadas de acordo com seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43589-105">Please note that these registry keys are only intended to be used internally by Windows Installer and they should not be relied upon by your application.</span></span> <span data-ttu-id="43589-106">O conteúdo, o local e a estrutura das informações armazenadas nessas chaves estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="43589-106">The content, location, and structure of information stored in these keys is subject to change.</span></span> <span data-ttu-id="43589-107">Os aplicativos devem depender do [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) para gerenciar assemblies.</span><span class="sxs-lookup"><span data-stu-id="43589-107">Applications should rely upon [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to manage assemblies.</span></span>

<span data-ttu-id="43589-108">Os assemblies são registrados por seus nomes de assembly.</span><span class="sxs-lookup"><span data-stu-id="43589-108">Assemblies are registered by their assembly names.</span></span> <span data-ttu-id="43589-109">Os nomes dos valores armazenados nos locais a seguir são os nomes de assembly.</span><span class="sxs-lookup"><span data-stu-id="43589-109">The names of the values stored in the following locations are the assembly names.</span></span> <span data-ttu-id="43589-110">Os valores reais são do tipo REG \_ multi \_ sz e contêm dados usados pelo [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) para instalar ou reparar assemblies.</span><span class="sxs-lookup"><span data-stu-id="43589-110">The actual values are of the type REG\_MULTI\_SZ and contain data used by [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to install or repair assemblies.</span></span>

## <a name="information-about-private-assemblies"></a><span data-ttu-id="43589-111">Informações sobre assemblies privados</span><span class="sxs-lookup"><span data-stu-id="43589-111">Information About Private Assemblies</span></span>

<span data-ttu-id="43589-112">Windows Installer armazena informações sobre assemblies privados transmitidos por Windows Installer pacotes que foram instalados como aplicativos gerenciados por usuário na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="43589-112">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="43589-113">**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Instalador** \\ do **Gerenciado** \\ **SID *_\\_* de usuário** Caminho dos assemblies do instalador para o \\  \\ \* *_arquivo de configuração_* _</span><span class="sxs-lookup"><span data-stu-id="43589-113">**HKLM**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Installer**\\**Managed**\\**_User SID_*_\\_\* Installer**\\**Assemblies**\\**_path to config file_* _</span></span>

<span data-ttu-id="43589-114">Windows Installer armazena informações sobre assemblies privados transmitidos por Windows Installer pacotes que foram instalados por usuário na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="43589-114">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="43589-115">_*HKCU **\\** software **\\** Microsoft **\\** Installer **\\** assemblies **\\** _caminho para o arquivo de configuração_*_</span><span class="sxs-lookup"><span data-stu-id="43589-115">_*HKCU **\\** Software **\\** Microsoft **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

<span data-ttu-id="43589-116">Windows Installer armazena informações sobre assemblies privados transportados por pacotes Windows Installer e instalados por computador na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="43589-116">Windows Installer stores information about private assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="43589-117">_*HKLM **\\** o **\\** caminho dos assemblies do **\\** instalador **\\** de classes de software para o **\\** _arquivo de configuração_*_</span><span class="sxs-lookup"><span data-stu-id="43589-117">_*HKLM **\\** SOFTWARE **\\** Classes **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

## <a name="information-about-global-or-shared-assemblies"></a><span data-ttu-id="43589-118">Informações sobre assemblies globais ou compartilhados</span><span class="sxs-lookup"><span data-stu-id="43589-118">Information About Global or Shared Assemblies</span></span>

<span data-ttu-id="43589-119">Windows Installer armazena informações sobre assemblies compartilhados transmitidos por Windows Installer pacotes que foram instalados como aplicativos gerenciados por usuário na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="43589-119">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="43589-120">_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\** _User Sid_*_ \\ _ *Installer **\\** assemblies **\\** global*\*</span><span class="sxs-lookup"><span data-stu-id="43589-120">_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\**_User SID_*_\\_ *Installer **\\** Assemblies **\\** Global*\*</span></span>

<span data-ttu-id="43589-121">Windows Installer armazena informações sobre assemblies compartilhados transmitidos por Windows Installer pacotes que foram instalados por usuário na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="43589-121">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="43589-122">**HKCU** \\ **Software** \\ **Microsoft** \\ **Instalador** \\ do **Assemblies** \\ do **Global**</span><span class="sxs-lookup"><span data-stu-id="43589-122">**HKCU**\\**Software**\\**Microsoft**\\**Installer**\\**Assemblies**\\**Global**</span></span>

<span data-ttu-id="43589-123">Windows Installer armazena informações sobre assemblies compartilhados transmitidos por Windows Installer pacotes e instalados por computador na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="43589-123">Windows Installer stores information about shared assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="43589-124">**HKLM** \\ **Software** \\ **Classes** \\ do **Instalador** \\ do **Assemblies** \\ do **Global**</span><span class="sxs-lookup"><span data-stu-id="43589-124">**HKLM**\\**SOFTWARE**\\**Classes**\\**Installer**\\**Assemblies**\\**Global**</span></span>

 

 



