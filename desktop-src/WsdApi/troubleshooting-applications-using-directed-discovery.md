---
description: Os aplicativos que usam a descoberta direcionada enviam mensagens de investigação por HTTP ou HTTPS para descobrir dispositivos.
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: Solução de problemas de aplicativos WSDAPI usando a descoberta direcionada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505701"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a><span data-ttu-id="ffea1-103">Solução de problemas de aplicativos WSDAPI usando a descoberta direcionada</span><span class="sxs-lookup"><span data-stu-id="ffea1-103">Troubleshooting WSDAPI Applications Using Directed Discovery</span></span>

<span data-ttu-id="ffea1-104">Os aplicativos que usam a descoberta direcionada enviam mensagens de [investigação](probe-message.md) por http ou HTTPS para descobrir dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ffea1-104">Applications that use directed discovery send [Probe](probe-message.md) messages over HTTP or HTTPS to discover devices.</span></span> <span data-ttu-id="ffea1-105">As mensagens [ProbeMatches](probematches-message.md) correspondentes enviadas em resposta também são enviadas por http ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ffea1-105">The corresponding [ProbeMatches](probematches-message.md) messages sent in response are also sent over HTTP or HTTPS.</span></span> <span data-ttu-id="ffea1-106">A descoberta direcionada pode ser iniciada pelo Assistente para adicionar impressora, um cliente de descoberta de função ou um aplicativo WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ffea1-106">Directed discovery can be initiated by the Add Printer Wizard, a Function Discovery client, or a WSDAPI application.</span></span> <span data-ttu-id="ffea1-107">As mensagens de investigação e ProbeMatches são estruturalmente idênticas às enviadas por UDP.</span><span class="sxs-lookup"><span data-stu-id="ffea1-107">The Probe and ProbeMatches messages are structurally identical to those sent over UDP.</span></span> <span data-ttu-id="ffea1-108">As mensagens são prefixadas com os cabeçalhos HTTP ou HTTPS apropriados.</span><span class="sxs-lookup"><span data-stu-id="ffea1-108">The messages are prefixed with the appropriate HTTP or HTTPS headers.</span></span>

<span data-ttu-id="ffea1-109">Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com um aplicativo usando a descoberta direcionada.</span><span class="sxs-lookup"><span data-stu-id="ffea1-109">The following diagnostic procedures should be used (in order) to help identify problems with an application using directed discovery.</span></span>

<span data-ttu-id="ffea1-110">**Para solucionar problemas de um aplicativo WSDAPI usando a descoberta direcionada**</span><span class="sxs-lookup"><span data-stu-id="ffea1-110">**To troubleshoot a WSDAPI application using directed discovery**</span></span>

1.  <span data-ttu-id="ffea1-111">[Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="ffea1-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="ffea1-112">[Use um host genérico e um cliente para a troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="ffea1-112">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
3.  <span data-ttu-id="ffea1-113">[Use o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="ffea1-113">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
4.  <span data-ttu-id="ffea1-114">[Inspecione os rastreamentos de rede de um aplicativo usando a descoberta direcionada](inspecting-network-traces-for-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="ffea1-114">[Inspect network traces for an application using directed discovery](inspecting-network-traces-for-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="ffea1-115">Se a origem do problema não puder ser identificada usando os procedimentos de diagnóstico acima, siga as instruções em [habilitando o rastreamento de WSDAPI](enabling-wsdapi-tracing.md) e entre em contato com o suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ffea1-115">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffea1-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ffea1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffea1-117">Introdução com a solução de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="ffea1-117">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="ffea1-118">Solução de problemas do assistente para adicionar impressora</span><span class="sxs-lookup"><span data-stu-id="ffea1-118">Troubleshooting the Add Printer Wizard</span></span>](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[<span data-ttu-id="ffea1-119">Solução de problemas de aplicativos WSDAPI</span><span class="sxs-lookup"><span data-stu-id="ffea1-119">Troubleshooting WSDAPI Applications</span></span>](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 



