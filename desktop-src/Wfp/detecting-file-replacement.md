---
description: O Proteção de Recursos do Windows (WRP) impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais instalados como parte do Windows Vista ou do Windows Server 2008.
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: Detectando substituição de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1855b98ca5834ef9e13e2f48bf7cca492e94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662992"
---
# <a name="detecting-resource-replacement"></a><span data-ttu-id="f850b-103">Detectando substituição de recursos</span><span class="sxs-lookup"><span data-stu-id="f850b-103">Detecting Resource Replacement</span></span>

<span data-ttu-id="f850b-104">O Proteção de Recursos do Windows (WRP) impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais instalados como parte do Windows Vista ou do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f850b-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of Windows Vista or Windows Server 2008.</span></span>

<span data-ttu-id="f850b-105">A WRP protege arquivos, pastas e chaves do registro no Windows Vista ou no Windows Server 2008, detectando e impedindo tentativas de substituição de recursos protegidos.</span><span class="sxs-lookup"><span data-stu-id="f850b-105">WRP protects files, folders, and registry keys on Windows Vista or Windows Server 2008 by detecting and preventing attempts to replace protected resources.</span></span> <span data-ttu-id="f850b-106">Essa proteção baseia-se em uma DACL (lista de controle de acesso discricional) do Windows e ACLs (listas de controle de acesso) definidas para recursos protegidos.</span><span class="sxs-lookup"><span data-stu-id="f850b-106">This protection is based on a Windows discretionary access control list (DACL) and access control lists (ACL) defined for protected resources.</span></span> <span data-ttu-id="f850b-107">Permissão para acesso completo para modificar recursos protegidos por WRP é restrita a TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="f850b-107">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="f850b-108">Os recursos protegidos por WRP só podem ser alterados usando os [mecanismos de substituição de recursos com suporte](supported-file-replacement-mechanisms.md) com o serviço instalador de módulos do Windows.</span><span class="sxs-lookup"><span data-stu-id="f850b-108">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="f850b-109">Os aplicativos que tentam modificar um recurso protegido por WRP nunca alteram o recurso e podem receber uma mensagem de erro que indica que o acesso ao recurso foi negado.</span><span class="sxs-lookup"><span data-stu-id="f850b-109">Applications attempting to modify a WRP-protected resource never change the resource and may receive an error message that states that access to the resource was denied.</span></span>

<span data-ttu-id="f850b-110">Os aplicativos e instaladores podem usar as funções [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) e [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) para determinar se um arquivo ou chave do registro está protegido.</span><span class="sxs-lookup"><span data-stu-id="f850b-110">Applications and installers can use the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) functions to determine whether a file or registry key is protected.</span></span>

<span data-ttu-id="f850b-111">\* \* Windows Server 2003 e Windows XP: \* \*</span><span class="sxs-lookup"><span data-stu-id="f850b-111">\*\*Windows Server 2003 and Windows XP:  \*\*</span></span>

<span data-ttu-id="f850b-112">A WFP (proteção de arquivo do Windows) protege os arquivos do sistema detectando tentativas de substituição de arquivos protegidos do sistema.</span><span class="sxs-lookup"><span data-stu-id="f850b-112">Windows File Protection (WFP) protects system files by detecting attempts to replace protected system files.</span></span> <span data-ttu-id="f850b-113">Essa proteção é disparada depois que a WFP recebe uma notificação de alteração de diretório para um arquivo em um diretório protegido.</span><span class="sxs-lookup"><span data-stu-id="f850b-113">This protection is triggered after WFP receives a directory change notification for a file in a protected directory.</span></span> <span data-ttu-id="f850b-114">Quando a WFP recebe essa notificação, ela determina qual arquivo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="f850b-114">When WFP receives this notification, it determines which file has changed.</span></span> <span data-ttu-id="f850b-115">Se o arquivo estiver protegido, a WFP pesquisará a assinatura do arquivo em um arquivo de catálogo para determinar se o novo arquivo é a versão correta.</span><span class="sxs-lookup"><span data-stu-id="f850b-115">If the file is protected, WFP looks up the file signature in a catalog file to determine if the new file is the correct version.</span></span> <span data-ttu-id="f850b-116">Se a versão do arquivo não estiver correta, o sistema substituirá o arquivo pela versão correta da mídia de cache ou de distribuição, dependendo se o arquivo está localizado no cache.</span><span class="sxs-lookup"><span data-stu-id="f850b-116">If the file version is not correct, the system replaces the file with the correct version from either the cache or distribution media, depending on whether the file is located in the cache.</span></span> <span data-ttu-id="f850b-117">A WFP procura o arquivo correto na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="f850b-117">WFP searches for the correct file in the following order:</span></span>

1.  <span data-ttu-id="f850b-118">Pesquise o diretório de cache.</span><span class="sxs-lookup"><span data-stu-id="f850b-118">Search the cache directory.</span></span>
2.  <span data-ttu-id="f850b-119">Pesquise o caminho de instalação de rede, se o sistema tiver sido instalado usando a instalação de rede.</span><span class="sxs-lookup"><span data-stu-id="f850b-119">Search the network install path, if the system was installed using network install.</span></span>
3.  <span data-ttu-id="f850b-120">Pesquise em um CD-ROM do Windows, se o sistema tiver sido instalado do CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="f850b-120">Search on a Windows CD-ROM, if the system was installed from CD-ROM.</span></span>

<span data-ttu-id="f850b-121">Se a WFP não conseguir localizar automaticamente o arquivo nos dois primeiros locais, ele exibirá a seguinte mensagem:</span><span class="sxs-lookup"><span data-stu-id="f850b-121">If WFP cannot automatically find the file in the first two locations, it displays the following message:</span></span>

![mensagem WFP exibida quando o arquivo não foi encontrado no diretório de cache ou no caminho de instalação de rede](images/wfp-1.png)

<span data-ttu-id="f850b-123">Se o sistema tiver sido instalado usando um CD-ROM, a WFP exibirá a seguinte mensagem:</span><span class="sxs-lookup"><span data-stu-id="f850b-123">If the system was installed using a CD-ROM, WFP displays the following message:</span></span>

![mensagem WFP exibida para solicitar que o usuário insira o CD-ROM do Windows](images/wfp-2.png)

<span data-ttu-id="f850b-125">Se um administrador não estiver conectado, a WFP não poderá exibir nenhuma dessas caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f850b-125">If an administrator is not logged on, WFP cannot display either of these dialog boxes.</span></span> <span data-ttu-id="f850b-126">A WFP exibirá a caixa de diálogo depois que um administrador fizer logon.</span><span class="sxs-lookup"><span data-stu-id="f850b-126">WFP will display the dialog box after an administrator logs on.</span></span>

<span data-ttu-id="f850b-127">A WFP também registra a tentativa de substituição de arquivo no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="f850b-127">WFP also logs the file replacement attempt in the system event log.</span></span> <span data-ttu-id="f850b-128">Se o administrador cancelou a restauração do arquivo correto, a WFP registra o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="f850b-128">If the administrator canceled restoration of the correct file, WFP logs the cancellation.</span></span>

## <a name="retrieving-the-list-of-protected-files"></a><span data-ttu-id="f850b-129">Recuperando a lista de arquivos protegidos</span><span class="sxs-lookup"><span data-stu-id="f850b-129">Retrieving the List of Protected Files</span></span>

<span data-ttu-id="f850b-130">O exemplo a seguir mostra como os aplicativos e instaladores podem usar a função [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) para obter a lista completa de arquivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="f850b-130">The following example shows how applications and installers can use the [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) function to get the complete list of protected files.</span></span>


```C++
#include <windows.h>
#include <sfc.h>
#include <stdio.h>

#pragma comment(lib, "sfc")

void wmain (int argc, WCHAR ** argv)
{  UNREFERENCED_PARAMETER(argc);    
   PROTECTED_FILE_DATA pfd = {0};
   BOOL fResult;

   wprintf (L"List of protected files:\n\n", argv[1]);

   while (FALSE != (fResult = SfcGetNextProtectedFile (NULL, &pfd)))
   {
      wprintf (L"   %lu   %s\n", pfd.FileNumber, pfd.FileName);
   }

   if (GetLastError() == ERROR_NO_MORE_FILES)
   {
      wprintf (L"\nAll %lu protected files listed\n", pfd.FileNumber);
   }
   else
   {
      wprintf (L"\nerror %lu: SfcGetNextProtectedFile() failed unexpectedly\n", GetLastError());
   }

}
```



 

 



