---
description: O Proteção de Recursos do Windows (WRP) impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais que são instalados como parte do sistema operacional.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: Sobre Proteção de Recursos do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c102225a547c4e454c3fb67ac94f715cd3adf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761086"
---
# <a name="about-windows-resource-protection"></a><span data-ttu-id="52f0a-103">Sobre Proteção de Recursos do Windows</span><span class="sxs-lookup"><span data-stu-id="52f0a-103">About Windows Resource Protection</span></span>

<span data-ttu-id="52f0a-104">O Proteção de Recursos do Windows (WRP) impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais que são instalados como parte do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="52f0a-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="52f0a-105">Ele se tornou disponível a partir do Windows Server 2008 e do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52f0a-105">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="52f0a-106">Permissão para acesso completo para modificar recursos protegidos por WRP é restrita a TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="52f0a-106">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="52f0a-107">Os recursos protegidos por WRP só podem ser alterados usando os [mecanismos de substituição de recursos com suporte](supported-file-replacement-mechanisms.md) com o serviço instalador de módulos do Windows.</span><span class="sxs-lookup"><span data-stu-id="52f0a-107">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="52f0a-108">A proteção desses recursos impede falhas de aplicativos e do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="52f0a-108">Protecting these resources prevents application and operating system failures.</span></span>

<span data-ttu-id="52f0a-109">Os aplicativos não devem tentar modificar os recursos protegidos por WRP porque eles são usados pelo Windows e por outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="52f0a-109">Applications should not attempt to modify WRP-protected resources because these are used by Windows and other applications.</span></span> <span data-ttu-id="52f0a-110">Se um aplicativo tentar modificar um recurso protegido por WRP, ele poderá ter os seguintes resultados.</span><span class="sxs-lookup"><span data-stu-id="52f0a-110">If an application attempts to modify a WRP-protected resource, it can have the following results.</span></span>

-   <span data-ttu-id="52f0a-111">Instaladores de aplicativos que tentam substituir, modificar ou excluir arquivos críticos do Windows ou chaves do registro podem falhar ao instalar o aplicativo e receberão uma mensagem de erro informando que o acesso ao recurso foi negado.</span><span class="sxs-lookup"><span data-stu-id="52f0a-111">Application installers that attempt to replace, modify, or delete critical Windows files or registry keys may fail to install the application and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="52f0a-112">Os aplicativos que tentam adicionar ou remover subchaves ou alterar os valores das chaves de registro protegidas podem falhar e receberão uma mensagem de erro informando que o acesso ao recurso foi negado.</span><span class="sxs-lookup"><span data-stu-id="52f0a-112">Applications that attempt to add or remove sub-keys or change the values of protected registry keys may fail and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="52f0a-113">Os aplicativos que dependem de gravar qualquer informação em chaves, pastas ou arquivos protegidos do registro podem falhar.</span><span class="sxs-lookup"><span data-stu-id="52f0a-113">Applications that rely on writing any information into protected registry keys, folders, or files may fail.</span></span>

<span data-ttu-id="52f0a-114">WRP é o novo nome da WFP (proteção de arquivo do Windows).</span><span class="sxs-lookup"><span data-stu-id="52f0a-114">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="52f0a-115">A WRP protege chaves e pastas do registro, bem como arquivos essenciais do sistema.</span><span class="sxs-lookup"><span data-stu-id="52f0a-115">WRP protects registry keys and folders as well as essential system files.</span></span> <span data-ttu-id="52f0a-116">A WFP estava disponível no Microsoft Windows Server 2003 e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="52f0a-116">WFP was available in Microsoft Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="52f0a-117">A WRP substitui a WFP no Windows Server 2008 e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52f0a-117">WRP replaces WFP in Windows Server 2008 and Windows Vista.</span></span>

<span data-ttu-id="52f0a-118">Os tópicos a seguir descrevem a WRP:</span><span class="sxs-lookup"><span data-stu-id="52f0a-118">The following topics describe WRP:</span></span>

-   [<span data-ttu-id="52f0a-119">Lista de recursos protegidos</span><span class="sxs-lookup"><span data-stu-id="52f0a-119">Protected Resource List</span></span>](protected-file-list.md)
-   [<span data-ttu-id="52f0a-120">Detectando substituição de recursos</span><span class="sxs-lookup"><span data-stu-id="52f0a-120">Detecting Resource Replacement</span></span>](detecting-file-replacement.md)
-   [<span data-ttu-id="52f0a-121">Mecanismos de substituição de recursos com suporte</span><span class="sxs-lookup"><span data-stu-id="52f0a-121">Supported Resource Replacement Mechanisms</span></span>](supported-file-replacement-mechanisms.md)
-   [<span data-ttu-id="52f0a-122">Verificador de arquivos do sistema</span><span class="sxs-lookup"><span data-stu-id="52f0a-122">System File Checker</span></span>](system-file-checker.md)
-   [<span data-ttu-id="52f0a-123">Considerações sobre administração remota</span><span class="sxs-lookup"><span data-stu-id="52f0a-123">Remote Administration Considerations</span></span>](remote-administration-considerations.md)

 

 



