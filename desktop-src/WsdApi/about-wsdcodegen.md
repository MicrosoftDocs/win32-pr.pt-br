---
description: Descreve os arquivos de entrada consumidos por WsdCodeGen e os arquivos de saída gerados pelo WsdCodeGen.
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: Sobre o WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010814"
---
# <a name="about-wsdcodegen"></a><span data-ttu-id="cb96d-103">Sobre o WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="cb96d-103">About WsdCodeGen</span></span>

<span data-ttu-id="cb96d-104">O WsdCodeGen usa um arquivo de configuração XML para determinar o local dos metadados do serviço.</span><span class="sxs-lookup"><span data-stu-id="cb96d-104">WsdCodeGen uses an XML configuration file to determine the location of the service metadata.</span></span> <span data-ttu-id="cb96d-105">O arquivo de configuração também é usado para definir nomes de interface, GUIDs de interface, nomes de classe, nomes de método e outros identificadores.</span><span class="sxs-lookup"><span data-stu-id="cb96d-105">The configuration file is also used to define interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> <span data-ttu-id="cb96d-106">Para obter mais informações sobre esse arquivo, consulte [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="cb96d-106">For more information about this file, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md).</span></span>

<span data-ttu-id="cb96d-107">O WsdCodeGen requer dois tipos de arquivos de entrada: um arquivo de configuração XML e um ou mais arquivos de descrição de serviço (arquivos WSDL e/ou XSD).</span><span class="sxs-lookup"><span data-stu-id="cb96d-107">WsdCodeGen requires two types of input files: an XML configuration file and one or more service description files (WSDL and/or XSD files).</span></span> <span data-ttu-id="cb96d-108">O WsdCodeGen processa esses arquivos de entrada e gera dois tipos de arquivos de saída: Arquivos de interface e arquivos de cabeçalho/origem.</span><span class="sxs-lookup"><span data-stu-id="cb96d-108">WsdCodeGen processes these input files and generates two type of output files: interface files and header/source files.</span></span>

## <a name="input-files"></a><span data-ttu-id="cb96d-109">Arquivos de entrada</span><span class="sxs-lookup"><span data-stu-id="cb96d-109">Input Files</span></span>



| <span data-ttu-id="cb96d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb96d-110">Type</span></span>                      | <span data-ttu-id="cb96d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb96d-111">Description</span></span>                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb96d-112">Arquivo de configuração</span><span class="sxs-lookup"><span data-stu-id="cb96d-112">Configuration file</span></span>        | <span data-ttu-id="cb96d-113">Um arquivo XML que indica o local dos metadados do serviço e define nomes de interface, GUIDs de interface, nomes de classe, nomes de método e outros identificadores.</span><span class="sxs-lookup"><span data-stu-id="cb96d-113">An XML file that indicates the location of the service metadata and defines interface names, interface GUIDs, class names, method names, and other identifiers.</span></span> |
| <span data-ttu-id="cb96d-114">Arquivos de descrição de serviço</span><span class="sxs-lookup"><span data-stu-id="cb96d-114">Service description files</span></span> | <span data-ttu-id="cb96d-115">Um ou mais arquivos WSDL ou XSD que descrevem os serviços a serem implementados no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cb96d-115">One or more WSDL or XSD files that describes the services to implement on the device.</span></span>                                                                           |



 

## <a name="output-files"></a><span data-ttu-id="cb96d-116">Arquivos de saída</span><span class="sxs-lookup"><span data-stu-id="cb96d-116">Output Files</span></span>



| <span data-ttu-id="cb96d-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb96d-117">Type</span></span>                        | <span data-ttu-id="cb96d-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb96d-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb96d-119">Arquivos de interface</span><span class="sxs-lookup"><span data-stu-id="cb96d-119">Interface files</span></span>             | <span data-ttu-id="cb96d-120">Um arquivo IDL (linguagem de definição de interface) que pode ser usado com o compilador MIDL para produzir um arquivo de cabeçalho de interface.</span><span class="sxs-lookup"><span data-stu-id="cb96d-120">An IDL (Interface Definition Language) file that can be used with the MIDL compiler to produce an interface header file.</span></span> <span data-ttu-id="cb96d-121">Os clientes WSDAPI e os serviços WSDAPI podem usar esse arquivo de interface.</span><span class="sxs-lookup"><span data-stu-id="cb96d-121">WSDAPI clients and WSDAPI services can use this interface file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="cb96d-122">Arquivos de cabeçalho e origem do C++</span><span class="sxs-lookup"><span data-stu-id="cb96d-122">C++ header and source files</span></span> | <span data-ttu-id="cb96d-123">Arquivos C++ que descrevem o contrato de mensagem, o namespace e as informações de tipo.</span><span class="sxs-lookup"><span data-stu-id="cb96d-123">C++ files that describe the message contract, namespace, and type information.</span></span> <span data-ttu-id="cb96d-124">Eles podem conter código de proxy e/ou código stub.</span><span class="sxs-lookup"><span data-stu-id="cb96d-124">They may contain proxy code and/or stub code.</span></span> <span data-ttu-id="cb96d-125">O código do proxy implementa a interface de um serviço e traduz as chamadas de método de serviço em operações WSDAPI que fazem solicitações de serviço.</span><span class="sxs-lookup"><span data-stu-id="cb96d-125">Proxy code implements a service's interface and translates service method calls into WSDAPI operations that make service requests.</span></span> <span data-ttu-id="cb96d-126">O código stub converte solicitações de serviço WSDAPI em código que chama métodos de serviço.</span><span class="sxs-lookup"><span data-stu-id="cb96d-126">Stub code translates WSDAPI service requests into code that calls service methods.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cb96d-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb96d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb96d-128">Serviços Web no gerador de código de dispositivos</span><span class="sxs-lookup"><span data-stu-id="cb96d-128">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="cb96d-129">Usando WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="cb96d-129">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 



