---
title: Ferramenta de compilador do WsUtil
description: A ferramenta do compilador do Windows Web Services, WsUtil.exe, dá suporte ao modelo de serviço e à serialização de tipos de dados. Ele processa documentos WSDL, de esquema XML e de política e gera cabeçalhos C e arquivos de origem.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Serviços Web da ferramenta de compilador WsUtil para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917798"
---
# <a name="wsutil-compiler-tool"></a><span data-ttu-id="5bc7e-107">Ferramenta de compilador do WsUtil</span><span class="sxs-lookup"><span data-stu-id="5bc7e-107">WsUtil Compiler tool</span></span>

<span data-ttu-id="5bc7e-108">A ferramenta do compilador do Windows Web Services, WsUtil.exe, dá suporte ao [modelo de serviço](service-model-layer-overview.md) e à [serialização](serialization.md) de tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-108">The Windows Web Services compiler tool, WsUtil.exe, supports the [service model](service-model-layer-overview.md) and [serialization](serialization.md) of data types.</span></span> <span data-ttu-id="5bc7e-109">Ele processa documentos WSDL, de esquema XML e de política e gera cabeçalhos C e arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-109">It processes WSDL, XML schema and policy documents, and generates C headers and source files.</span></span> <span data-ttu-id="5bc7e-110">Essa ferramenta é semelhante à ferramenta de compilador WSDL para código gerenciado, mas é destinada a código nativo em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-110">This tool is similar to WSDL compiler tool for managed code but is aimed at native code instead.</span></span>

<span data-ttu-id="5bc7e-111">Para dar suporte ao [modelo de serviço](service-model-layer-overview.md), WsUtil.exe gera cabeçalhos a serem usados tanto para o cliente quanto para o serviço.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-111">To support the [service model](service-model-layer-overview.md), WsUtil.exe generates headers to be used for both client and service.</span></span> <span data-ttu-id="5bc7e-112">Ele gera o arquivo de proxy C para o lado do cliente e os arquivos stub C para o lado do serviço, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-112">It generates C proxy file for the client side, and C stub files for the service side, as needed.</span></span>

<span data-ttu-id="5bc7e-113">Para dar suporte à [serialização](serialization.md), o compilador gera cabeçalhos para as descrições de elemento para definições de elementos globais e todas as informações de definição de tipo nos arquivos de proxy consumidos pelo mecanismo de serialização.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-113">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all the type definition information in the proxy files that is consumed by the serialization engine.</span></span>


<span data-ttu-id="5bc7e-114">Para obter opções de linha de comando para processar arquivos WSDL, arquivos de esquema XML e arquivos de política de serviço Web, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="5bc7e-114">For command line options for processing WSDL files, XML Schema files, and web service policy files, see the following topics:</span></span>

-   [<span data-ttu-id="5bc7e-115">Ferramenta de compilador de serviço Web</span><span class="sxs-lookup"><span data-stu-id="5bc7e-115">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
-   [<span data-ttu-id="5bc7e-116">Contratos de serviço e WSDL</span><span class="sxs-lookup"><span data-stu-id="5bc7e-116">WSDL and Service Contracts</span></span>](wsdl-support.md)
-   [<span data-ttu-id="5bc7e-117">Suporte de esquema</span><span class="sxs-lookup"><span data-stu-id="5bc7e-117">Schema support</span></span>](schema-support.md)
-   [<span data-ttu-id="5bc7e-118">Suporte de política</span><span class="sxs-lookup"><span data-stu-id="5bc7e-118">Policy support</span></span>](policy-support.md)

## <a name="security"></a><span data-ttu-id="5bc7e-119">Segurança</span><span class="sxs-lookup"><span data-stu-id="5bc7e-119">Security</span></span>

<span data-ttu-id="5bc7e-120">Ao usar o WsUtil, esteja atento aos seguintes problemas e observe as precauções apropriadas:</span><span class="sxs-lookup"><span data-stu-id="5bc7e-120">When you use WsUtil, be aware of the following issues and observe the appropriate precautions:</span></span>

-   <span data-ttu-id="5bc7e-121">Wsutil não recupera metadados XML pela rede e Wsutil não resolve as instruções import e/ou include nos arquivos de metadados de entrada.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-121">Wsutil does not retrieve XML metadata over the network, and wsutil does not resolve import and/or include statements in the input metadata files.</span></span> <span data-ttu-id="5bc7e-122">Wsutil abre e lê arquivos WSDL, XSD e de política.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-122">Wsutil opens and reads wsdl, xsd, and policy files.</span></span> <span data-ttu-id="5bc7e-123">Os metadados XML não são resistentes a adulterações.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-123">XML metadata is not tamper resistant.</span></span> <span data-ttu-id="5bc7e-124">Certifique-se de usar somente arquivos WSDL, XSD e de política são adquiridos da fonte confiável e certifique-se de proteger os arquivos contra violação antes e depois de usá-los.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-124">Ensure that you only use wsdl, xsd and policy files are acquired from trusted source and make sure to protect the files from tampering before and after using them.</span></span> <span data-ttu-id="5bc7e-125">Examine atentamente o conteúdo dos arquivos de entrada e valide se o conteúdo dos arquivos é seguro para uso no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-125">Carefully review the contents of the input files and validate that the contents of files are safe for use in the application.</span></span> <span data-ttu-id="5bc7e-126">Wsutil.exe não realiza nenhuma verificação de autenticidade dos arquivos de metadados.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-126">Wsutil.exe does not do any verification of authenticity of the metadata files.</span></span>
-   <span data-ttu-id="5bc7e-127">O Wsutil gera arquivos de cabeçalho e stub, que não são resistentes a adulterações.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-127">Wsutil generates header and stub files, which are not tamper resistant.</span></span> <span data-ttu-id="5bc7e-128">Você precisa definir os direitos de acesso de nível correto em arquivos de origem gerados pelo wsutil.exe para impedir o acesso unauthoritized a esses arquivos.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-128">You need to set the correct level access rights on source files generated by wsutil.exe to prevent unauthoritized access to those files.</span></span> <span data-ttu-id="5bc7e-129">Wsutil usa System. IO. StreamWriter para criar os arquivos de saída.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-129">Wsutil uses System.IO.StreamWriter to create the output files.</span></span>
-   <span data-ttu-id="5bc7e-130">Os usuários precisam estar cientes de que o Wsutil pode substituir seus arquivos locais e deve ter cuidado para especificar nomes de arquivos e diretórios seguros para arquivos de saída usando a opção/out.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-130">Users need to be aware that Wsutil can overwrite their local files, and they should be careful to specify safe file names and directories for output files using the /out switch.</span></span>
-   <span data-ttu-id="5bc7e-131">Wsutil ou wsutilhelper.dll carregado na wsutil.exe, pode ser encerrado inesperadamente ou consumir uma grande quantidade de recursos do sistema quando estiver sob ataque ou no processamento de uma quantidade muito grande de metadados de entrada.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-131">Wsutil or wsutilhelper.dll loaded in wsutil.exe, may terminate unexpectedly or consume large amount of system resources when under attack or in processing a very large amount of input metadata.</span></span> <span data-ttu-id="5bc7e-132">A ferramenta foi projetada para ser usada durante o tempo de desenvolvimento apenas essa ferramenta deve ser usada apenas como uma ferramenta de tempo de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-132">The tool is designed to be used during development time only This tool should be used as a development time tool only.</span></span> <span data-ttu-id="5bc7e-133">Ele pode não ser seguro para uso na camada intermediária para processar informações de política.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-133">It may not be safe for use in the middle tier to process policy information.</span></span>
-   <span data-ttu-id="5bc7e-134">Wsutilhelper.dll DLL auxiliar é carregado em wsutil.exe gerenciado para processar informações de política.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-134">Wsutilhelper.dll helper DLL is loaded into managed wsutil.exe to process policy information.</span></span> <span data-ttu-id="5bc7e-135">O usuário deve garantir que nenhum binário mal-intencionado com o mesmo nome de arquivo exista no caminho binário.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-135">User should make sure no malicious binary with same filename exists in the binary path.</span></span> <span data-ttu-id="5bc7e-136">Da mesma forma, o usuário deve ter certeza no ambiente de compilação, o caminho binário está configurado corretamente, pois não há nenhum binário mal-intencionado com o mesmo nome "wsutil.exe".</span><span class="sxs-lookup"><span data-stu-id="5bc7e-136">Similarly, user should make sure in the build environment, the binary path is setup correctly that there is no malicious binary with same "wsutil.exe" name exists.</span></span>
-   <span data-ttu-id="5bc7e-137">O Wsutil gera a anotação SAL para os campos de operações e estrutura quando possível.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-137">Wsutil generates SAL annotation for operations and structure fields when possible.</span></span> <span data-ttu-id="5bc7e-138">O usuário de arquivos gerados pelo Wsutil deve seguir o requisito especificado por meio da anotação SAL.</span><span class="sxs-lookup"><span data-stu-id="5bc7e-138">User of wsutil generated files should follow the requirement specified through SAL annotation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bc7e-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bc7e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bc7e-140">Visão geral da camada do modelo de serviço</span><span class="sxs-lookup"><span data-stu-id="5bc7e-140">Service Model Layer Overview</span></span>](service-model-layer-overview.md)
</dt> <dt>

[<span data-ttu-id="5bc7e-141">Série</span><span class="sxs-lookup"><span data-stu-id="5bc7e-141">Serialization</span></span>](serialization.md)
</dt> <dt>

[<span data-ttu-id="5bc7e-142">Ferramenta de compilador de serviço Web</span><span class="sxs-lookup"><span data-stu-id="5bc7e-142">Web Service Compiler Tool</span></span>](web-service-compiler-tool.md)
</dt> <dt>

[<span data-ttu-id="5bc7e-143">Suporte a WSDL</span><span class="sxs-lookup"><span data-stu-id="5bc7e-143">WSDL support</span></span>](wsdl-support.md)
</dt> <dt>

[<span data-ttu-id="5bc7e-144">Suporte de esquema</span><span class="sxs-lookup"><span data-stu-id="5bc7e-144">Schema support</span></span>](schema-support.md)
</dt> <dt>

[<span data-ttu-id="5bc7e-145">Suporte de política</span><span class="sxs-lookup"><span data-stu-id="5bc7e-145">Policy Support</span></span>](policy-support.md)
</dt> </dl>

 

 




