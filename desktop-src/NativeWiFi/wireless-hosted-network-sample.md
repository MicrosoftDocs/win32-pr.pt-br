---
description: Demonstra o uso de funções de rede hospedadas sem fio.
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: Exemplo de rede hospedada sem fio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775680"
---
# <a name="wireless-hosted-network-sample"></a><span data-ttu-id="1f836-103">Exemplo de rede hospedada sem fio</span><span class="sxs-lookup"><span data-stu-id="1f836-103">Wireless Hosted Network Sample</span></span>

<span data-ttu-id="1f836-104">Um exemplo de rede hospedada sem fio que demonstra o uso de funções de rede hospedadas sem fio está incluído no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1f836-104">A wireless Hosted Network sample that demonstrates the use of wireless Hosted Network functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1f836-105">A versão mais recente do SDK do Windows está disponível no [centro de download](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span><span class="sxs-lookup"><span data-stu-id="1f836-105">The latest version of the Windows SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span>

<span data-ttu-id="1f836-106">Por padrão, o código-fonte do exemplo de rede hospedada sem fio é instalado no seguinte diretório:</span><span class="sxs-lookup"><span data-stu-id="1f836-106">By default, the wireless Hosted Network sample source code is installed in the following directory:</span></span>

<span data-ttu-id="1f836-107">**C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ NetDs \\ WLAN**</span><span class="sxs-lookup"><span data-stu-id="1f836-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="1f836-108">O exemplo de rede hospedada sem fio está localizado na seguinte pasta:</span><span class="sxs-lookup"><span data-stu-id="1f836-108">The wireless Hosted Network sample is located under the following folder:</span></span>

<span data-ttu-id="1f836-109">**WirelessHostedNetwork**</span><span class="sxs-lookup"><span data-stu-id="1f836-109">**WirelessHostedNetwork**</span></span>

<span data-ttu-id="1f836-110">O exemplo de rede hospedada sem fio pode ser compilado no SDK do Windows para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1f836-110">The Wireless Hosted Network sample can be compiled on the Windows SDK for Windows 7.</span></span> <span data-ttu-id="1f836-111">O exemplo de rede hospedada sem fio pode ser executado no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado.</span><span class="sxs-lookup"><span data-stu-id="1f836-111">The Wireless Hosted Network sample can be run on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span>

<span data-ttu-id="1f836-112">No Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado, o sistema operacional instalará um dispositivo virtual se um adaptador sem fio compatível com a rede hospedada estiver presente no computador.</span><span class="sxs-lookup"><span data-stu-id="1f836-112">On Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine.</span></span> <span data-ttu-id="1f836-113">Esse dispositivo virtual normalmente aparece na "pasta Conexões de rede" como "conexão de rede sem fio 2" com um nome de dispositivo "adaptador de miniporta WiFi virtual da Microsoft" se o computador tiver um único adaptador de rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="1f836-113">This virtual device normally shows up in the "Network Connections Folder" as "Wireless Network Connection 2" with a Device Name of "Microsoft Virtual WiFi Miniport adapter" if the computer has a single wireless network adapter.</span></span> <span data-ttu-id="1f836-114">Este dispositivo virtual é usado exclusivamente para executar conexões de SoftAP (ponto de acesso de software).</span><span class="sxs-lookup"><span data-stu-id="1f836-114">This virtual device is used exclusively for performing software access point (SoftAP) connections.</span></span> <span data-ttu-id="1f836-115">O tempo de vida desse dispositivo virtual está vinculado ao adaptador sem fio físico.</span><span class="sxs-lookup"><span data-stu-id="1f836-115">The lifetime of this virtual device is tied to the physical wireless adapter.</span></span> <span data-ttu-id="1f836-116">Se o adaptador sem fio físico estiver desabilitado, esse dispositivo virtual também será removido.</span><span class="sxs-lookup"><span data-stu-id="1f836-116">If the physical wireless adapter is disabled, this virtual device will be removed as well.</span></span>

<span data-ttu-id="1f836-117">As funções de rede hospedada sem fio são usadas para iniciar e parar a rede hospedada sem fio, definir ou alterar as configurações ou consultar informações.</span><span class="sxs-lookup"><span data-stu-id="1f836-117">The wireless Hosted Network functions are used to start and stop the wireless Hosted Network, configure or change settings, or query for information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f836-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f836-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f836-119">Sobre a rede hospedada sem fio</span><span class="sxs-lookup"><span data-stu-id="1f836-119">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="1f836-120">Usando rede hospedada e compartilhamento de conexão com a Internet</span><span class="sxs-lookup"><span data-stu-id="1f836-120">Using Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[<span data-ttu-id="1f836-121">**WlanHostedNetworkForceStart**</span><span class="sxs-lookup"><span data-stu-id="1f836-121">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[<span data-ttu-id="1f836-122">**WlanHostedNetworkInitSettings**</span><span class="sxs-lookup"><span data-stu-id="1f836-122">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[<span data-ttu-id="1f836-123">**WlanHostedNetworkQueryProperty**</span><span class="sxs-lookup"><span data-stu-id="1f836-123">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[<span data-ttu-id="1f836-124">**WlanHostedNetworkQuerySecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="1f836-124">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[<span data-ttu-id="1f836-125">**WlanHostedNetworkQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="1f836-125">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[<span data-ttu-id="1f836-126">**WlanHostedNetworkRefreshSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="1f836-126">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[<span data-ttu-id="1f836-127">**WlanHostedNetworkSetProperty**</span><span class="sxs-lookup"><span data-stu-id="1f836-127">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[<span data-ttu-id="1f836-128">**WlanHostedNetworkSetSecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="1f836-128">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[<span data-ttu-id="1f836-129">**WlanHostedNetworkStartUsing**</span><span class="sxs-lookup"><span data-stu-id="1f836-129">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[<span data-ttu-id="1f836-130">**WlanHostedNetworkStopUsing**</span><span class="sxs-lookup"><span data-stu-id="1f836-130">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[<span data-ttu-id="1f836-131">**WlanRegisterVirtualStationNotification**</span><span class="sxs-lookup"><span data-stu-id="1f836-131">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 



