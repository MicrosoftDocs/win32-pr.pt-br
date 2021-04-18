---
description: As ferramentas de desenvolvimento do WSDAPI incluídas no SDK do Windows (WSD CodeGen, host de depuração WSD e cliente de depuração WSD) permitem que os desenvolvedores criem e depurem clientes e dispositivos baseados em WSDAPI.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Ferramentas de desenvolvimento do WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793296"
---
# <a name="wsdapi-development-tools"></a><span data-ttu-id="602a2-103">Ferramentas de desenvolvimento do WSDAPI</span><span class="sxs-lookup"><span data-stu-id="602a2-103">WSDAPI Development Tools</span></span>

<span data-ttu-id="602a2-104">As ferramentas de desenvolvimento do WSDAPI incluídas no SDK do Windows (WSD CodeGen, host de depuração WSD e cliente de depuração WSD) permitem que os desenvolvedores criem e depurem clientes e dispositivos baseados em WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="602a2-104">The WSDAPI development tools included in the Windows SDK (WSD CodeGen, WSD Debug Host, and WSD Debug Client) enable developers to create and debug WSDAPI-based clients and devices.</span></span> <span data-ttu-id="602a2-105">O código-fonte para essas ferramentas não está disponível.</span><span class="sxs-lookup"><span data-stu-id="602a2-105">The source code for these tools is not available.</span></span> <span data-ttu-id="602a2-106">As ferramentas do SDK estão localizadas no seguinte diretório: <Windows SDK Install Folder> \\ bin.</span><span class="sxs-lookup"><span data-stu-id="602a2-106">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="602a2-107">WSD CodeGen (wsdcodegen.exe) converte um contrato WSDL no código C++ gerado, que os desenvolvedores podem chamar diretamente no.</span><span class="sxs-lookup"><span data-stu-id="602a2-107">WSD CodeGen (wsdcodegen.exe) converts a WSDL contract into generated C++ code, which developers can call directly into.</span></span> <span data-ttu-id="602a2-108">Ele lida com a serialização de dados e a representação de transmissão para que os desenvolvedores possam se concentrar na criação de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="602a2-108">It handles the data serialization and wire representation so developers can focus on designing applications.</span></span> <span data-ttu-id="602a2-109">Para obter mais informações sobre WSD CodeGen, consulte [Serviços Web no gerador de código de dispositivos](web-services-for-devices-code-generator.md).</span><span class="sxs-lookup"><span data-stu-id="602a2-109">For more information about WSD CodeGen, see [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="602a2-110">Essa ferramenta está disponível no Microsoft Windows Software Development Kit (SDK) e no Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="602a2-110">This tool is available in the Microsoft Windows Software Development Kit (SDK) and in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="602a2-111">As ferramentas de host de depuração WSD (wsddebug \_host.exe) e de cliente de depuração WSD (wsddebug \_client.exe) ajudam os desenvolvedores a depurar seus clientes e hosts.</span><span class="sxs-lookup"><span data-stu-id="602a2-111">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools help developers debug their clients and hosts.</span></span> <span data-ttu-id="602a2-112">Essas ferramentas podem ser usadas para verificar e inspecionar o tráfego de WS-Discovery e de troca de metadados.</span><span class="sxs-lookup"><span data-stu-id="602a2-112">These tools can be used to verify and inspect WS-Discovery and metadata exchange traffic.</span></span> <span data-ttu-id="602a2-113">Para obter mais informações sobre o host de depuração WSD e o cliente de depuração WSD, consulte [ferramentas de depuração](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="602a2-113">For more information about WSD Debug Host and WSD Debug Client, see [Debugging Tools](debugging-tools.md).</span></span> <span data-ttu-id="602a2-114">Essas ferramentas estão disponíveis apenas no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="602a2-114">These tools are available only in the Windows SDK.</span></span>

<span data-ttu-id="602a2-115">Há uma ferramenta de desenvolvimento adicional chamada [WSDBIT (ferramenta de interoperabilidade básica do WSDAPI)](https://msdn.microsoft.com/library/cc264250.aspx), que está disponível apenas no WDK.</span><span class="sxs-lookup"><span data-stu-id="602a2-115">There is an additional development tool, named [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), that is available only in the WDK.</span></span> <span data-ttu-id="602a2-116">Essa ferramenta é usada para testar métodos de serviço, MTOM (mecanismo de otimização de transmissão de mensagens), anexos ou WS-Eventing.</span><span class="sxs-lookup"><span data-stu-id="602a2-116">This tool is used for testing service methods, Message Transmission Optimization Mechanism (MTOM), attachments or WS-Eventing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="602a2-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="602a2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="602a2-118">Desenvolvimento de aplicativos WSD no Windows</span><span class="sxs-lookup"><span data-stu-id="602a2-118">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="602a2-119">Serviços Web no gerador de código de dispositivos</span><span class="sxs-lookup"><span data-stu-id="602a2-119">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="602a2-120">Ferramenta de interoperabilidade básica do WSDAPI (WSDBIT)</span><span class="sxs-lookup"><span data-stu-id="602a2-120">WSDAPI Basic Interoperability Tool (WSDBIT)</span></span>](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[<span data-ttu-id="602a2-121">Ferramentas de depuração</span><span class="sxs-lookup"><span data-stu-id="602a2-121">Debugging Tools</span></span>](debugging-tools.md)
</dt> </dl>

 

 



