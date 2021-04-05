---
description: Exemplos de Winsock avançados usando extensões de soquete seguro
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Exemplos de Winsock avançados usando extensões de soquete seguro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6701809ad97c7d39acf1f0eae646e7555e5c967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920912"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a><span data-ttu-id="023d7-103">Exemplos de Winsock avançados usando extensões de soquete seguro</span><span class="sxs-lookup"><span data-stu-id="023d7-103">Advanced Winsock Samples Using Secure Socket Extensions</span></span>

## <a name="secure-tcp-client-and-server-sample"></a><span data-ttu-id="023d7-104">Exemplo de cliente e servidor de TCP seguro</span><span class="sxs-lookup"><span data-stu-id="023d7-104">Secure TCP Client and Server Sample</span></span>

<span data-ttu-id="023d7-105">Um exemplo de Winsock mais avançado que demonstra o uso de extensões de soquete seguro está incluído no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="023d7-105">A more advanced Winsock sample that demonstrates the use of secure socket extensions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="023d7-106">O exemplo inclui um cliente TCP e um servidor que se conectam com segurança usando o Winsock e as extensões de soquete seguro.</span><span class="sxs-lookup"><span data-stu-id="023d7-106">The sample includes a TCP client and server that connect securely using the Winsock and the secure socket extensions.</span></span>

<span data-ttu-id="023d7-107">Por padrão, o código-fonte de exemplo do Winsock é instalado no seguinte diretório:</span><span class="sxs-lookup"><span data-stu-id="023d7-107">By default, the Winsock sample source code is installed in the following directory:</span></span>

<span data-ttu-id="023d7-108">*C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ amostras \\ NetDs \\ Winsock*</span><span class="sxs-lookup"><span data-stu-id="023d7-108">*C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\NetDs\\winsock*</span></span>

<span data-ttu-id="023d7-109">Um exemplo está localizado na seguinte pasta:</span><span class="sxs-lookup"><span data-stu-id="023d7-109">A sample is located under the following folder:</span></span>

<span data-ttu-id="023d7-110">*securesocket*</span><span class="sxs-lookup"><span data-stu-id="023d7-110">*securesocket*</span></span>

<span data-ttu-id="023d7-111">O código de exemplo é dividido em diretórios separados, conforme descrito abaixo:</span><span class="sxs-lookup"><span data-stu-id="023d7-111">The sample code is split into separate directories as described below:</span></span>

-   <span data-ttu-id="023d7-112">stcpclient-a pasta que contém o código de cliente TCP seguro.</span><span class="sxs-lookup"><span data-stu-id="023d7-112">stcpclient - the folder that contains the secure TCP client code.</span></span>
-   <span data-ttu-id="023d7-113">stcpcommon-a pasta que contém o código de biblioteca comum que é compartilhado entre o cliente e o servidor de TCP seguro.</span><span class="sxs-lookup"><span data-stu-id="023d7-113">stcpcommon - the folder that contains common library code that is shared between the secure TCP client and server.</span></span>
-   <span data-ttu-id="023d7-114">stcpserver-a pasta que contém o código do servidor TCP seguro.</span><span class="sxs-lookup"><span data-stu-id="023d7-114">stcpserver - the folder that contains the secure TCP server code.</span></span>

<span data-ttu-id="023d7-115">Deve-se observar que os exemplos devem ser executados em dois computadores diferentes que executam o Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="023d7-115">It should be noted that the samples are meant to be run on two different computers running Windows Vista or later.</span></span> <span data-ttu-id="023d7-116">Além disso, as credenciais IPsec devem ser provisionadas em ambos os computadores para que a conexão seja realizada com sucesso, pois o exemplo usa IPsec para proteger seu tráfego.</span><span class="sxs-lookup"><span data-stu-id="023d7-116">Additionally, IPsec credentials must be provisioned on both the computers for the connection to succeed, because the sample uses IPsec for securing its traffic.</span></span> <span data-ttu-id="023d7-117">Consulte a documentação sobre configuração de [IPSec](/windows/desktop/FWP/ipsec-configuration) para obter mais informações sobre como configurar credenciais IPSec.</span><span class="sxs-lookup"><span data-stu-id="023d7-117">Please refer to the documentation on [IPsec Configuration](/windows/desktop/FWP/ipsec-configuration) for more information on setting up IPsec credentials.</span></span>

<span data-ttu-id="023d7-118">A criação do exemplo irá gerar dois arquivos executáveis:</span><span class="sxs-lookup"><span data-stu-id="023d7-118">Building the sample will generate two executable files:</span></span>

<span data-ttu-id="023d7-119">*stcpclient.exe* e *stcpserver.exe*.</span><span class="sxs-lookup"><span data-stu-id="023d7-119">*stcpclient.exe* and *stcpserver.exe*.</span></span>

<span data-ttu-id="023d7-120">Copie *stcpclient.exe* para o computador a e copie *stcpserver.exe* para o computador B. No computador B, inicie o servidor TCP executando o seguinte em um prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="023d7-120">Copy *stcpclient.exe* to computer A and copy *stcpserver.exe* to computer B. On computer B, start the TCP server by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="023d7-121">**stcpserver.exe**</span><span class="sxs-lookup"><span data-stu-id="023d7-121">**stcpserver.exe**</span></span>

<span data-ttu-id="023d7-122">Execute o seguinte comando para obter mais opções de uso para o servidor:</span><span class="sxs-lookup"><span data-stu-id="023d7-122">Execute the following command for more usage options for the server:</span></span>

<span data-ttu-id="023d7-123">**stcpserver.exe/?**</span><span class="sxs-lookup"><span data-stu-id="023d7-123">**stcpserver.exe /?**</span></span>

<span data-ttu-id="023d7-124">Em seguida, no computador A, inicie o cliente TCP executando o seguinte em um prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="023d7-124">Then on computer A, start the TCP client by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="023d7-125">**stcpclient.exe <totalmente qualificado-DNS-name-for-Machine-B>**</span><span class="sxs-lookup"><span data-stu-id="023d7-125">**stcpclient.exe <fully-qualified-DNS-name-for-machine-B>**</span></span>

<span data-ttu-id="023d7-126">Neste ponto, a conexão deve ser estabelecida com segurança.</span><span class="sxs-lookup"><span data-stu-id="023d7-126">At this point the connection should get established securely.</span></span>

<span data-ttu-id="023d7-127">Execute o seguinte comando para obter mais opções de uso para o cliente:</span><span class="sxs-lookup"><span data-stu-id="023d7-127">Execute the following command for more usage options for the client:</span></span>

<span data-ttu-id="023d7-128">**stcpclient.exe/?**</span><span class="sxs-lookup"><span data-stu-id="023d7-128">**stcpclient.exe /?**</span></span>

## <a name="related-topics"></a><span data-ttu-id="023d7-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="023d7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="023d7-130">Sobre a plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="023d7-130">About Windows Filtering Platform</span></span>](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[<span data-ttu-id="023d7-131">Aplicação da camada de aplicativo (EPA)</span><span class="sxs-lookup"><span data-stu-id="023d7-131">Application Layer Enforcement (ALE)</span></span>](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[<span data-ttu-id="023d7-132">Configuração de IPsec</span><span class="sxs-lookup"><span data-stu-id="023d7-132">IPsec Configuration</span></span>](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[<span data-ttu-id="023d7-133">Funções IPsec</span><span class="sxs-lookup"><span data-stu-id="023d7-133">IPsec Functions</span></span>](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[<span data-ttu-id="023d7-134">Usando extensões de soquete seguro</span><span class="sxs-lookup"><span data-stu-id="023d7-134">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="023d7-135">SSPI (interface do provedor de suporte de segurança)</span><span class="sxs-lookup"><span data-stu-id="023d7-135">Security Support Provider Interface (SSPI)</span></span>](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[<span data-ttu-id="023d7-136">Plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="023d7-136">Windows Filtering Platform</span></span>](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[<span data-ttu-id="023d7-137">Funções da API da Windows Filtering Platform</span><span class="sxs-lookup"><span data-stu-id="023d7-137">Windows Filtering Platform API Functions</span></span>](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[<span data-ttu-id="023d7-138">Extensões do Winsock Secure Socket</span><span class="sxs-lookup"><span data-stu-id="023d7-138">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
