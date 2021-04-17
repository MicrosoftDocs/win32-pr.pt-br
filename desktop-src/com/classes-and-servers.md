---
title: Classes e servidores
description: Classes e servidores
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366764"
---
# <a name="classes-and-servers"></a><span data-ttu-id="f2244-103">Classes e servidores</span><span class="sxs-lookup"><span data-stu-id="f2244-103">Classes and Servers</span></span>

<span data-ttu-id="f2244-104">COM usa **a \_ \_ raiz de classes hKey** para configurações de todo o computador, mas também permite a configuração por usuário de CLSIDs para maior segurança e flexibilidade.</span><span class="sxs-lookup"><span data-stu-id="f2244-104">COM uses **HKEY\_CLASSES\_ROOT** for computer-wide settings but also allows per-user configuration of CLSIDS for greater security and flexibility.</span></span> <span data-ttu-id="f2244-105">O COM primeiro consulta o **HKEY \_ Current \_ user \\ software \\ classes** antes de examinar a **\_ \_ raiz de classes hKey**.</span><span class="sxs-lookup"><span data-stu-id="f2244-105">COM first consults **HKEY\_CURRENT\_USER\\Software\\Classes** before looking under **HKEY\_CLASSES\_ROOT**.</span></span> <span data-ttu-id="f2244-106">O COM mantém informações em todo o computador relacionadas a CLSIDs em classe **HKEY \_ \_ raiz \\ CLSID** e mantém as informações de classes por usuário em **HKEY \_ Current \_ user \\ software \\ classes \\ CLSID**.</span><span class="sxs-lookup"><span data-stu-id="f2244-106">COM keeps computer-wide information related to CLSIDs under **HKEY\_CLASSES\_ROOT\\CLSID** and keeps per-user class information under **HKEY\_CURRENT\_USER\\Software\\Classes\\CLSID**.</span></span>

<span data-ttu-id="f2244-107">Os servidores COM oferecem suporte ao auto-registro.</span><span class="sxs-lookup"><span data-stu-id="f2244-107">COM servers support self-registration.</span></span> <span data-ttu-id="f2244-108">Para um servidor em processo, isso significa que a DLL deve exportar as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="f2244-108">For an in-process server, this means that the DLL must export the following functions:</span></span>

-   [<span data-ttu-id="f2244-109">**DllRegisterServer**</span><span class="sxs-lookup"><span data-stu-id="f2244-109">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [<span data-ttu-id="f2244-110">**DllUnregisterServer**</span><span class="sxs-lookup"><span data-stu-id="f2244-110">**DllUnregisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

<span data-ttu-id="f2244-111">Você deve exportar explicitamente essas funções usando um arquivo de definição de módulo, opções de vinculador ou diretivas de compilador.</span><span class="sxs-lookup"><span data-stu-id="f2244-111">You must explicitly export these functions by using a module definition file, linker switches, or compiler directives.</span></span> <span data-ttu-id="f2244-112">O repositório de classe usa essas funções para configurar o registro local depois de baixar o arquivo para o computador cliente.</span><span class="sxs-lookup"><span data-stu-id="f2244-112">The class store uses these functions to configure the local registry after downloading the file to the client machine.</span></span> <span data-ttu-id="f2244-113">Além do armazenamento de classe, essas funções também são usadas por outros ambientes para instalar servidores em computadores host.</span><span class="sxs-lookup"><span data-stu-id="f2244-113">In addition to class store, these functions are also used by other environments to install servers on host computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2244-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2244-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2244-115">Registrando aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="f2244-115">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 