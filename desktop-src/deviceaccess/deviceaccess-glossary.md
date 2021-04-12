---
title: Glossário de acesso ao dispositivo
description: Veja a seguir os termos usados em toda a documentação da API de acesso ao dispositivo.
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365513"
---
# <a name="device-access-glossary"></a><span data-ttu-id="6426a-103">Glossário de acesso ao dispositivo</span><span class="sxs-lookup"><span data-stu-id="6426a-103">Device Access Glossary</span></span>

<span data-ttu-id="6426a-104">Veja a seguir os termos usados em toda a documentação da API de acesso ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6426a-104">The following are terms used throughout the documentation for the Device Access API.</span></span>

<dl> <dt>

<span data-ttu-id="6426a-105">**Contêiner**</span><span class="sxs-lookup"><span data-stu-id="6426a-105">**AppContainer**</span></span>
</dt> <dd>

<span data-ttu-id="6426a-106">Um ambiente de execução altamente restrito no qual um processo é executado com um subconjunto reduzido dos privilégios do usuário.</span><span class="sxs-lookup"><span data-stu-id="6426a-106">A highly restricted execution environment in which a process runs with a reduced subset of the user's privileges.</span></span> <span data-ttu-id="6426a-107">Um processo em execução em um AppContainer é chamado de processo de AppContainer.</span><span class="sxs-lookup"><span data-stu-id="6426a-107">A process that's running within an AppContainer is called an AppContainer process.</span></span> <span data-ttu-id="6426a-108">Um processo do AppContainer é isolado de outros processos do AppContainer e do perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="6426a-108">An AppContainer process is isolated from other AppContainer processes and from the user's profile.</span></span> <span data-ttu-id="6426a-109">Ele tem acesso limitado a um subconjunto muito pequeno de recursos do sistema, como arquivos, dispositivos, chaves do registro, pontos de extremidade de RPC (chamada de procedimento) e recursos de rede de IPC (comunicação entre processos).</span><span class="sxs-lookup"><span data-stu-id="6426a-109">It has limited access to a very small subset of system resources like files, devices, registry keys, interprocess communication (IPC)/remote procedure call (RPC) endpoints, and network resources.</span></span>

</dd> <dt>

<span data-ttu-id="6426a-110">**Associação**</span><span class="sxs-lookup"><span data-stu-id="6426a-110">**Binding**</span></span>
</dt> <dd>

<span data-ttu-id="6426a-111">Associar um objeto de acesso de dispositivo a uma interface de dispositivo específica.</span><span class="sxs-lookup"><span data-stu-id="6426a-111">Associating a device access object with a particular device interface.</span></span> <span data-ttu-id="6426a-112">Se a associação for bem-sucedida, os aplicativos da Windows Store poderão usar o objeto de acesso ao dispositivo como um agente para se comunicar com o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6426a-112">If binding is successful, Windows Store apps can use the device access object as a broker to communicate with the device driver.</span></span>

</dd> <dt>

<span data-ttu-id="6426a-113">**Agente**</span><span class="sxs-lookup"><span data-stu-id="6426a-113">**Broker**</span></span>
</dt> <dd>

<span data-ttu-id="6426a-114">Um componente que fornece acesso a um recurso que não é concedido por padrão.</span><span class="sxs-lookup"><span data-stu-id="6426a-114">A component that provides access to a resource that isn't granted by default.</span></span>

</dd> <dt>

<span data-ttu-id="6426a-115">**Aplicativo privilegiado**</span><span class="sxs-lookup"><span data-stu-id="6426a-115">**Privileged App**</span></span>
</dt> <dd>

<span data-ttu-id="6426a-116">Um aplicativo que é identificado em metadados de um dispositivo específico como associado a esse dispositivo, para que ele possa se comunicar com a interface restrita do driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6426a-116">An app that's identified in a particular device's metadata as associated with that device, so that it can communicate with the device driver's restricted interface.</span></span> <span data-ttu-id="6426a-117">Um exemplo desse aplicativo pode ser um aplicativo de reprodução de música proprietário que tem permissão exclusiva para sincronizar com um player portátil de música, quando os aplicativos de concorrentes não podem.</span><span class="sxs-lookup"><span data-stu-id="6426a-117">An example of such an app might be a proprietary music playback app that has exclusive permission to sync with a portable music player, when apps from competitors can't.</span></span> <span data-ttu-id="6426a-118">Para obter mais informações sobre como definir os metadados de um dispositivo ou como restringir um driver a aplicativos com privilégios, consulte [aplicativos de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span><span class="sxs-lookup"><span data-stu-id="6426a-118">For more information about how to set a device's metadata or how to restrict a driver to privileged apps, see [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices).</span></span>

</dd> </dl>
