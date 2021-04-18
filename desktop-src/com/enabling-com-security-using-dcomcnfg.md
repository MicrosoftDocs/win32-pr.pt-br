---
title: Habilitando a segurança COM usando DCOMCNFG
description: Dcomcnfg.exe fornece uma interface do usuário para modificar certas configurações no Registro.
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01139584b715fccdad923bc5eb3d6a863a63ef8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813227"
---
# <a name="enabling-com-security-using-dcomcnfg"></a><span data-ttu-id="41e3a-103">Habilitando a segurança COM usando DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="41e3a-103">Enabling COM Security Using DCOMCNFG</span></span>

<span data-ttu-id="41e3a-104">Dcomcnfg.exe fornece uma interface do usuário para modificar certas configurações no Registro.</span><span class="sxs-lookup"><span data-stu-id="41e3a-104">Dcomcnfg.exe provides a user interface for modifying certain settings in the registry.</span></span> <span data-ttu-id="41e3a-105">Usando Dcomcnfg.exe, você pode habilitar a segurança em todo o computador ou em todo o processo.</span><span class="sxs-lookup"><span data-stu-id="41e3a-105">By using Dcomcnfg.exe, you can enable security either on a computer-wide or a process-wide basis.</span></span> <span data-ttu-id="41e3a-106">Você pode habilitar a segurança para um computador específico para que, quando um processo não fornecer suas próprias configurações de segurança, seja de forma programática ou por meio de valores de registro, os valores definidos por Dcomcnfg.exe serão usados.</span><span class="sxs-lookup"><span data-stu-id="41e3a-106">You can enable security for a particular computer so that when a process does not provide its own security settings, either programmatically or through registry values, the values set by Dcomcnfg.exe will be used.</span></span> <span data-ttu-id="41e3a-107">Ou você pode usar Dcomcnfg.exe para habilitar a segurança apenas para um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="41e3a-107">Or you can use Dcomcnfg.exe to enable security for a particular application only.</span></span>

<span data-ttu-id="41e3a-108">Ao habilitar a segurança, há duas tarefas principais a serem realizadas:</span><span class="sxs-lookup"><span data-stu-id="41e3a-108">When enabling security, there are two primary tasks to accomplish:</span></span>

-   <span data-ttu-id="41e3a-109">Defina um nível de autenticação que não seja nenhum.</span><span class="sxs-lookup"><span data-stu-id="41e3a-109">Set an authentication level that is not None.</span></span>
-   <span data-ttu-id="41e3a-110">Defina permissões, incluindo as permissões de inicialização e de acesso.</span><span class="sxs-lookup"><span data-stu-id="41e3a-110">Set permissions, including both launch and access permissions.</span></span>

<span data-ttu-id="41e3a-111">As etapas executadas para realizar essas tarefas dependem se você está habilitando a segurança para todo o computador ou apenas para um determinado aplicativo.</span><span class="sxs-lookup"><span data-stu-id="41e3a-111">The steps taken to accomplish these tasks depend on whether you are enabling security for the whole computer or just for a particular application.</span></span> <span data-ttu-id="41e3a-112">Além disso, talvez você queira definir outros valores para o computador ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="41e3a-112">Also, you may want to set other values for the computer or application.</span></span>

> [!Note]  
> <span data-ttu-id="41e3a-113">Você deve ser um administrador para executar Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="41e3a-113">You must be an administrator to run Dcomcnfg.exe.</span></span>

 

<span data-ttu-id="41e3a-114">Os tópicos a seguir fornecem procedimentos passo a passo sobre como definir a segurança com Dcomcnfg.exe:</span><span class="sxs-lookup"><span data-stu-id="41e3a-114">The following topics provide step-by-step procedures on how to set security with Dcomcnfg.exe:</span></span>

-   [<span data-ttu-id="41e3a-115">Definindo System-Wide segurança usando DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="41e3a-115">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="41e3a-116">Configurando a segurança do processwide usando DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="41e3a-116">Setting Processwide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="41e3a-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41e3a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41e3a-118">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="41e3a-118">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="41e3a-119">Desativando a segurança</span><span class="sxs-lookup"><span data-stu-id="41e3a-119">Turning Off Security</span></span>](turning-off-security.md)
</dt> </dl>

 

 




