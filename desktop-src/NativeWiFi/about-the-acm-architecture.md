---
description: Sobre a arquitetura do ACM
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: Sobre a arquitetura do ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f037a1823f7045ccaf1dc573c6d213beeebe0a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171687"
---
# <a name="about-the-acm-architecture"></a><span data-ttu-id="d54fd-103">Sobre a arquitetura do ACM</span><span class="sxs-lookup"><span data-stu-id="d54fd-103">About the ACM Architecture</span></span>

<span data-ttu-id="d54fd-104">O módulo de configuração automática (ACM) é o novo componente de configuração sem fio para o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d54fd-104">The Auto Configuration Module (ACM) is the new wireless configuration component for Windows Vista.</span></span> <span data-ttu-id="d54fd-105">O Windows XP com Service Pack 3 (SP3) e a API de LAN sem fio para Windows XP com Service Pack 2 (SP2) usam o serviço WZC (Wireless Zero Configuration).</span><span class="sxs-lookup"><span data-stu-id="d54fd-105">Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) use the Wireless Zero Configuration (WZC) service instead.</span></span>

<span data-ttu-id="d54fd-106">O ACM verifica as redes periodicamente e usa um processo iterativo para selecionar e se conectar à rede mais preferencial no intervalo, se essa rede tiver uma interface habilitada para conexão automática.</span><span class="sxs-lookup"><span data-stu-id="d54fd-106">The ACM scans networks periodically and uses an iterative process to select and connect to the most preferred network in the range, if that network has an interface enabled for auto-connection.</span></span> <span data-ttu-id="d54fd-107">O ACM também salva e recupera perfis de rede, que contêm configurações do ACM, módulo específico de mídia (MSM), segurança e fornecedor de hardware independente (IHV).</span><span class="sxs-lookup"><span data-stu-id="d54fd-107">The ACM also saves and retrieves network profiles, which contain ACM, Media Specific Module (MSM), security, and independent hardware vendor (IHV) settings.</span></span> <span data-ttu-id="d54fd-108">Esses perfis de rede são para configuração automática.</span><span class="sxs-lookup"><span data-stu-id="d54fd-108">These network profiles are for auto configuration.</span></span>

<span data-ttu-id="d54fd-109">A configuração automática dá suporte a configurações globais e por interface e perfis de rede.</span><span class="sxs-lookup"><span data-stu-id="d54fd-109">Auto configuration supports both global and per-interface settings and network profiles.</span></span> <span data-ttu-id="d54fd-110">As configurações globais e os perfis de rede são configurados se o computador tiver ingressado em um domínio com um GPO (objeto de política de grupo) no nível de domínio ou no nível da UO (unidade organizacional) na hierarquia do Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="d54fd-110">The global settings and network profiles are configured if the machine has joined a domain with a group policy object (GPO) either at the domain level or the organizational unit (OU) level in the Active Directory (AD) hierarchy.</span></span> <span data-ttu-id="d54fd-111">Essas configurações e perfis de diretiva de grupo são somente leitura, aplicadas a cada interface 802,11 no sistema e sempre têm precedência sobre as configurações por interface e por usuário e os perfis de rede.</span><span class="sxs-lookup"><span data-stu-id="d54fd-111">These group policy settings and profiles are read-only, applied to each 802.11 interface in the system, and always take precedence over the per-interface and per-user settings and network profiles.</span></span> <span data-ttu-id="d54fd-112">Os perfis de política de grupo são colocados na parte superior da lista de perfil de rede preferencial em cada adaptador de rede 802,11.</span><span class="sxs-lookup"><span data-stu-id="d54fd-112">The group policy profiles are placed at the top of the preferred network profile list on each 802.11 network interface.</span></span>

<span data-ttu-id="d54fd-113">A arquitetura ACM é extensível.</span><span class="sxs-lookup"><span data-stu-id="d54fd-113">The ACM architecture is extensible.</span></span> <span data-ttu-id="d54fd-114">Os IHVs podem implementar a funcionalidade sem fio proprietária sem alterar a estrutura nativa 802,11 fornecida.</span><span class="sxs-lookup"><span data-stu-id="d54fd-114">IHVs can implement proprietary wireless functionality without altering the provided native 802.11 framework.</span></span> <span data-ttu-id="d54fd-115">As funções e estruturas de controle de IHV expostas habilitam essa extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="d54fd-115">The exposed IHV control functions and structures enable this extensibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d54fd-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d54fd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d54fd-117">Sobre WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="d54fd-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 



