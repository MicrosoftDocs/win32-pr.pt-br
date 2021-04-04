---
description: Há dois exemplos de WSDAPI incluídos no SDK do Windows para o Windows Server 2008.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: Exemplos de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed088c43f9617da062d5e4fb4f0343f74e3bcbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661746"
---
# <a name="wsdapi-samples"></a><span data-ttu-id="e50cb-103">Exemplos de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="e50cb-103">WSDAPI Samples</span></span>

<span data-ttu-id="e50cb-104">Há dois exemplos de WSDAPI incluídos no SDK do Windows para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e50cb-104">There are two WSDAPI samples included with the Windows SDK for Windows Server 2008.</span></span> <span data-ttu-id="e50cb-105">O código-fonte para os exemplos pode ser encontrado em <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="e50cb-105">The source code for the samples can be found in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI.</span></span> <span data-ttu-id="e50cb-106">Esta versão do SDK está disponível no centro de [Download](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span><span class="sxs-lookup"><span data-stu-id="e50cb-106">This version of the SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span> <span data-ttu-id="e50cb-107">Os exemplos não estão disponíveis no SDK do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e50cb-107">The samples are not available in the Windows Vista SDK.</span></span>

<span data-ttu-id="e50cb-108">O exemplo de cotação de ações (localizado em <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ StockQuote) demonstra um serviço com a funcionalidade de mensagens básica.</span><span class="sxs-lookup"><span data-stu-id="e50cb-108">The stock quote sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\StockQuote) demonstrates a service with basic messaging functionality.</span></span> <span data-ttu-id="e50cb-109">O exemplo de serviço de arquivo (localizado em <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ fileservice) demonstra um serviço com funcionalidade avançada, como mensagens assíncronas, anexos e eventos.</span><span class="sxs-lookup"><span data-stu-id="e50cb-109">The file service sample (located in <Windows SDK Install Folder>\\Samples\\Web\\WSDAPI\\FileService) demonstrates a service with advanced functionality, such as asynchronous messaging, attachments, and eventing.</span></span>

<span data-ttu-id="e50cb-110">Ambos os exemplos incluem os seguintes tipos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e50cb-110">Both samples include the following types of files.</span></span>

-   <span data-ttu-id="e50cb-111">Arquivos WSDL que contêm as descrições de serviço.</span><span class="sxs-lookup"><span data-stu-id="e50cb-111">WSDL files that contain the service descriptions.</span></span>
-   <span data-ttu-id="e50cb-112">[Arquivos de configuração WsdCodeGen](wsdcodegen-configuration-file.md) usados para gerar código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="e50cb-112">[WsdCodeGen configuration files](wsdcodegen-configuration-file.md) used to generate WSDAPI code.</span></span>
-   <span data-ttu-id="e50cb-113">Cabeçalhos e arquivos de origem gerados do C++.</span><span class="sxs-lookup"><span data-stu-id="e50cb-113">Generated C++ header and source files.</span></span>
-   <span data-ttu-id="e50cb-114">Arquivos de implementação de cliente e serviço.</span><span class="sxs-lookup"><span data-stu-id="e50cb-114">Client and service implementation files.</span></span>
-   <span data-ttu-id="e50cb-115">Arquivos de solução e projeto do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e50cb-115">Visual Studio project and solution files.</span></span>

<span data-ttu-id="e50cb-116">Ambos os exemplos implementam hosts de dispositivo ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), proxies de dispositivo ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) e proxies de serviço ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span><span class="sxs-lookup"><span data-stu-id="e50cb-116">Both samples implement device hosts ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), device proxies ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)), and service proxies ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)).</span></span> <span data-ttu-id="e50cb-117">Além disso, o exemplo de serviço de arquivo demonstra o uso de mensagens assíncronas ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), anexos ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) e eventos.</span><span class="sxs-lookup"><span data-stu-id="e50cb-117">In addition, the file service sample demonstrates the use of asynchronous messaging ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), attachments ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) and eventing.</span></span>

<span data-ttu-id="e50cb-118">Os arquivos FileServiceContract. vcproj e StockQuoteContract. vcproj incluídos com os exemplos chamam [WsdCodeGen](web-services-for-devices-code-generator.md) para gerar arquivos de cabeçalho e origem do C++ a partir do arquivo WSDL especificado no arquivo de configuração WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="e50cb-118">The FileServiceContract.vcproj and StockQuoteContract.vcproj files included with the samples call [WsdCodeGen](web-services-for-devices-code-generator.md) to generate C++ header and source files from the WSDL file specified in the WsdCodeGen configuration file.</span></span> <span data-ttu-id="e50cb-119">Isso significa que, se o arquivo de configuração WSDL ou WsdCodeGen de exemplo for alterado e o projeto de exemplo for recriado, o WsdCodeGen gerará automaticamente novos arquivos de cabeçalho e origem que refletem as alterações.</span><span class="sxs-lookup"><span data-stu-id="e50cb-119">This means that if the sample WSDL or WsdCodeGen configuration file is changed and the sample project is rebuilt, WsdCodeGen automatically generates new header and source files that reflect the changes.</span></span> <span data-ttu-id="e50cb-120">Esse é o método preferencial para a criação de aplicativos WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="e50cb-120">This is the preferred method for building WSDAPI applications.</span></span> <span data-ttu-id="e50cb-121">WsdCodeGen geralmente é chamado na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="e50cb-121">WsdCodeGen is usually called from the command line.</span></span> <span data-ttu-id="e50cb-122">Abra o \* arquivo. vcproj relevante para exibir as chamadas de linha de comando do WsdCodeGen de exemplo.</span><span class="sxs-lookup"><span data-stu-id="e50cb-122">Open the relevant \*.vcproj file to view the example WsdCodeGen command line calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e50cb-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e50cb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e50cb-124">Desenvolvimento de aplicativos WSD no Windows</span><span class="sxs-lookup"><span data-stu-id="e50cb-124">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



