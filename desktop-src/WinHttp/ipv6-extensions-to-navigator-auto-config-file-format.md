---
description: A Microsoft implementou uma matriz de extensões para o formato de arquivo de configuração automática do Navigator a fim de adicionar suporte a IPv6 nas funções auxiliares de WPAD do WinINet e do WinHTTP.
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: Formato de arquivo de configuração automática de extensões IPv6 para navegador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b57fce93caaf7790136ee9ac7db04017d9ac11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760427"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a><span data-ttu-id="ce3dd-103">Formato de arquivo de configuração automática de extensões IPv6 para navegador</span><span class="sxs-lookup"><span data-stu-id="ce3dd-103">IPv6 Extensions to Navigator Auto-Config File Format</span></span>

<span data-ttu-id="ce3dd-104">A Microsoft implementou uma matriz de extensões para o formato de arquivo de configuração automática do Navigator a fim de adicionar suporte a IPv6 nas funções auxiliares de WPAD do WinINet e do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="ce3dd-104">Microsoft has implemented an array of extensions to the Navigator Auto-Config File Format in order to add IPv6 support in the WinINet and WinHTTP WPAD helper functions.</span></span>

<span data-ttu-id="ce3dd-105">A explosão da Internet no final de 1990 causou um escassez inesperado de endereços IPv4, com o pool esgotado diariamente.</span><span class="sxs-lookup"><span data-stu-id="ce3dd-105">The explosion of the Internet in the late 1990’s has caused an unexpected scarcity of IPv4 addresses, with the pool depleting on a daily basis.</span></span> <span data-ttu-id="ce3dd-106">O IPv6 fornece uma solução para esse problema e, embora não esteja amplamente implantado, seu uso definitivamente se tornará mais predominante no futuro.</span><span class="sxs-lookup"><span data-stu-id="ce3dd-106">IPv6 provides a solution to this problem and although it is currently not widely deployed, its use will definitely become more prevalent in the future.</span></span> <span data-ttu-id="ce3dd-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) é um protocolo que permite que os clientes Web detectem automaticamente o que a configuração correta de proxy deve ser para o tráfego de saída.</span><span class="sxs-lookup"><span data-stu-id="ce3dd-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) is a protocol that allows web clients to automatically detect what the correct proxy configuration should be for their outgoing traffic.</span></span> <span data-ttu-id="ce3dd-108">Isso é muito útil para implantações corporativas porque permite que os administradores de ti configurem scripts complexos que podem rotear o tráfego para todos os clientes para proxies específicos com base no servidor de destino ao qual os clientes estão tentando se conectar.</span><span class="sxs-lookup"><span data-stu-id="ce3dd-108">This is very useful for corporate deployments because it allows IT administrators to setup complex scripts that can route traffic for all clients to specific proxies based on the target server the clients are attempting to connect to.</span></span> <span data-ttu-id="ce3dd-109">O WinINet e o WinHTTP dão suporte a funções auxiliares WPAD, conforme definido pela [especificação de formato de Arquivo PAC (configuração automática de proxy do navegador)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), que se tornou um padrão de fato.</span><span class="sxs-lookup"><span data-stu-id="ce3dd-109">WinINet and WinHTTP support WPAD helper functions as defined by the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), which has become a defacto standard.</span></span> <span data-ttu-id="ce3dd-110">Infelizmente, essa especificação foi escrita em 1996 e não define o que os comportamentos de função devem ser quando um script WPAD é implantado em uma rede compatível com IPv6.</span><span class="sxs-lookup"><span data-stu-id="ce3dd-110">Unfortunately this specification was written in 1996 and does not define what the function behaviors should be when a WPAD script is deployed in an IPv6 capable network.</span></span>

<span data-ttu-id="ce3dd-111">Como o IPv6 é a onda do futuro, todos os componentes do Windows agora oferecem suporte à pilha dupla (IPv4 e IPv6) e às redes IPv6.</span><span class="sxs-lookup"><span data-stu-id="ce3dd-111">Since IPv6 is the wave of the future, all Windows components now support dual stack (IPv4 and IPv6) and IPv6 only networks.</span></span> <span data-ttu-id="ce3dd-112">Para dar suporte a IPv6 sem afetar a implantação existente, a Microsoft adicionou 6 novas funções de classe auxiliar como uma extensão para a especificação de formato de Arquivo PAC (auto-config) do navegador e também adicionou uma nova função compatível com IPv6 chamada **FindProxyForURLEx** que os administradores podem implementar no script WPAD.</span><span class="sxs-lookup"><span data-stu-id="ce3dd-112">In order to support IPv6 without affecting existing deployment, Microsoft added 6 new helper class functions as an extension to the Navigator Proxy Auto-Config (PAC) File Format specification and also added a new IPv6 capable function called **FindProxyForURLEx** that administrators can implement in the WPAD script.</span></span>

<dl> <dt>

[<span data-ttu-id="ce3dd-113">Definições da API auxiliar de proxy com reconhecimento de IPv6</span><span class="sxs-lookup"><span data-stu-id="ce3dd-113">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[<span data-ttu-id="ce3dd-114">Diferenças entre IPv6-Aware funções auxiliares WPAD e funções auxiliares WPAD herdadas</span><span class="sxs-lookup"><span data-stu-id="ce3dd-114">Differences Between IPv6-Aware WPAD Helper Functions and Legacy WPAD Helper Functions</span></span>](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
<span data-ttu-id="ce3dd-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ce3dd-115"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="ce3dd-116">Essa funcionalidade requer o Windows Internet Explorer 7 ou superior.</span><span class="sxs-lookup"><span data-stu-id="ce3dd-116">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



