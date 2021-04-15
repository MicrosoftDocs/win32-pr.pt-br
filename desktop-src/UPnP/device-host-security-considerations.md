---
title: Considerações de segurança de host de dispositivo
description: O uso do host de dispositivo cria problemas de segurança.
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5a51b90bff33949a33cd9fa1046deb1916ab30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454136"
---
# <a name="device-host-security-considerations"></a><span data-ttu-id="aa493-103">Considerações de segurança de host de dispositivo</span><span class="sxs-lookup"><span data-stu-id="aa493-103">Device Host Security Considerations</span></span>

<span data-ttu-id="aa493-104">O uso do host de dispositivo cria problemas de segurança devido ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="aa493-104">Using the device host creates security issues because of the following:</span></span>

-   <span data-ttu-id="aa493-105">Os dispositivos hospedados em um computador que executa o Windows XP enviam anúncios em todas as redes.</span><span class="sxs-lookup"><span data-stu-id="aa493-105">Devices hosted on a computer running Windows XP sends announcements on all networks.</span></span>
-   <span data-ttu-id="aa493-106">Os dispositivos hospedados em um computador que executa o Windows XP permitem o controle de dispositivos de todas as redes.</span><span class="sxs-lookup"><span data-stu-id="aa493-106">Devices hosted on a computer running Windows XP allow control of devices from all networks.</span></span>

<span data-ttu-id="aa493-107">Isso aumenta o risco para os consumidores domésticos, pois dispositivos como um player de mídia ou um sistema HVAC ou de iluminação hospedado em um computador que executa o Windows XP estão visíveis e podem ser controlados a partir de pontos de controle fora do início.</span><span class="sxs-lookup"><span data-stu-id="aa493-107">This increases the risk to home consumers, because devices such as a media player or a bridged lighting or HVAC system hosted on a computer running Windows XP are visible and can be controlled from control points outside the home.</span></span>

<span data-ttu-id="aa493-108">Ao criar um dispositivo hospedado, você precisa levar em consideração alguns problemas de segurança.</span><span class="sxs-lookup"><span data-stu-id="aa493-108">When you are creating a hosted device, you need to take into consideration some security issues.</span></span>

-   <span data-ttu-id="aa493-109">Para reduzir o escopo de descoberta e ataque de dispositivos baseados em UPnP, a TTL de todas as mensagens SSDP é 1.</span><span class="sxs-lookup"><span data-stu-id="aa493-109">To reduce the scope of discovery and attack of UPnP-based devices, the TTL of all SSDP messages is 1.</span></span> <span data-ttu-id="aa493-110">Isso significa que um dispositivo registrado só é descoberto por pontos de controle na mesma rede.</span><span class="sxs-lookup"><span data-stu-id="aa493-110">This means that a registered device is only discovered by control points on the same network.</span></span> <span data-ttu-id="aa493-111">Você pode configurar uma TTL mais alta no registro.</span><span class="sxs-lookup"><span data-stu-id="aa493-111">You can configure a higher TTL in the registry.</span></span>
-   <span data-ttu-id="aa493-112">O registro de um dispositivo que não está em execução requer o registro prévio do Device. dll com COM, o que exige privilégio de administrador.</span><span class="sxs-lookup"><span data-stu-id="aa493-112">Registering a non-running device requires pre-registering the device .dll with COM, which requires administrator privilege.</span></span>
-   <span data-ttu-id="aa493-113">O registro de um dispositivo em execução requer privilégio de administrador, serviço local ou sistema local.</span><span class="sxs-lookup"><span data-stu-id="aa493-113">Registering a running device requires Administrator, Local Service, or Local System privilege.</span></span>
-   <span data-ttu-id="aa493-114">Quando o host do dispositivo é iniciado, ele é executado como [LocalService](/windows/desktop/Services/localservice-account).</span><span class="sxs-lookup"><span data-stu-id="aa493-114">When the device host is started, it is run as [LocalService](/windows/desktop/Services/localservice-account).</span></span> <span data-ttu-id="aa493-115">Isso dá ao dispositivo a capacidade de gerar auditorias e ler a chave do registro **HKEY \_ local \_ Machine** .</span><span class="sxs-lookup"><span data-stu-id="aa493-115">This gives the device the ability to generate audits and read the **HKEY\_LOCAL\_MACHINE** registry key.</span></span> <span data-ttu-id="aa493-116">O dispositivo tem acesso ao **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="aa493-116">The device does have access to **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="aa493-117">A conta LocalService pode usar recursos para os quais o LocalService recebeu acesso, bem como aqueles que concedem acesso ao AuthenticatedUser.</span><span class="sxs-lookup"><span data-stu-id="aa493-117">The LocalService account can use resources to which LocalService has been granted access, as well as those that grant access to AuthenticatedUser.</span></span> <span data-ttu-id="aa493-118">O dispositivo restringiu o acesso ao sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="aa493-118">The device has restricted file system access.</span></span>
-   <span data-ttu-id="aa493-119">As ACLs do sistema de arquivos devem ser atualizadas para permitir o acesso de [LocalService](/windows/desktop/Services/localservice-account) ao diretório de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa493-119">The file system ACLs must be updated to allow [LocalService](/windows/desktop/Services/localservice-account) access to the resource directory.</span></span>
-   <span data-ttu-id="aa493-120">Se o dispositivo precisar ter mais acesso de segurança, você poderá criar seu próprio processo para o dispositivo e registrá-lo usando [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).</span><span class="sxs-lookup"><span data-stu-id="aa493-120">If your device must have more security access, you can create your own process for the device and register it by using [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).</span></span>

 

 