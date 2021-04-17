---
title: Habilitando o registro em log
description: Habilitando o registro em log
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Windows Media Gerenciador de Dispositivos, registro em log
- Gerenciador de Dispositivos, registro em log
- aplicativos de área de trabalho, registro em log
- provedores de serviços, registro em log
- Guia de programação, registro em log
- registro em log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e95be13e93a5a58bb728d5600c6fdea9801ec2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813206"
---
# <a name="enabling-logging"></a><span data-ttu-id="24189-109">Habilitando o registro em log</span><span class="sxs-lookup"><span data-stu-id="24189-109">Enabling Logging</span></span>

<span data-ttu-id="24189-110">O Windows Media Gerenciador de Dispositivos fornece um objeto de log que pode salvar informações em um arquivo de texto em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="24189-110">Windows Media Device Manager provides a logging object that can save information to a text file at run time.</span></span> <span data-ttu-id="24189-111">Os desenvolvedores de aplicativos e provedores de serviços podem usar esse objeto para armazenar mensagens em um arquivo de log enquanto seu aplicativo ou provedor de serviços está em execução.</span><span class="sxs-lookup"><span data-stu-id="24189-111">Developers of both applications and service providers can use this object to store messages in a log file while their application or service provider is running.</span></span> <span data-ttu-id="24189-112">Esse objeto é especialmente útil ao manipular arquivos protegidos por DRM, porque o Windows Media Gerenciador de Dispositivos não permitirá que você anexe um depurador a um processo que esteja manipulando arquivos protegidos por DRM.</span><span class="sxs-lookup"><span data-stu-id="24189-112">This object is especially useful when handling DRM-protected files, because Windows Media Device Manager will not allow you to attach a debugger to a process that is handling DRM-protected files.</span></span>

<span data-ttu-id="24189-113">O agente é um objeto com com a ID de classe CLSID \_ WMDMLogger que expõe uma interface, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span><span class="sxs-lookup"><span data-stu-id="24189-113">The logger is a COM object with the class ID CLSID\_WMDMLogger that exposes one interface, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span> <span data-ttu-id="24189-114">Os componentes não precisam de um certificado para usar o objeto de log.</span><span class="sxs-lookup"><span data-stu-id="24189-114">Components do not need a certificate to use the logging object.</span></span>

<span data-ttu-id="24189-115">Por padrão, o Windows Media Gerenciador de Dispositivos mantém um arquivo de log, independentemente de um aplicativo usar **IWMDMLogger**.</span><span class="sxs-lookup"><span data-stu-id="24189-115">By default, Windows Media Device Manager maintains a log file, regardless of whether an application uses **IWMDMLogger**.</span></span> <span data-ttu-id="24189-116">Esse arquivo de log é um arquivo de texto simples, e cada entrada inclui uma entrada precedida por um carimbo de data/hora no formato AAAAMMDDHHMMSS, usando a hora local de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="24189-116">This log file is a simple text file, and each entry includes an entry preceded by a time stamp in the format YYYYMMDDHHMMSS, using 24-hour local time.</span></span> <span data-ttu-id="24189-117">O Windows Media Gerenciador de Dispositivos registra todas as chamadas à API, juntamente com as entradas que você adiciona chamando mensagens **IWMDMLogger** .</span><span class="sxs-lookup"><span data-stu-id="24189-117">Windows Media Device Manager logs all API calls, along with any entries you add by calling **IWMDMLogger** messages.</span></span> <span data-ttu-id="24189-118">Todas as entradas do arquivo de log são anexadas ao arquivo até que a [**redefinição**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) seja chamada ou o arquivo exceda seu tamanho máximo.</span><span class="sxs-lookup"><span data-stu-id="24189-118">All log file entries are appended to the file until [**Reset**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) is called, or the file exceeds its maximum size.</span></span> <span data-ttu-id="24189-119">O arquivo é fechado automaticamente após cada operação de log.</span><span class="sxs-lookup"><span data-stu-id="24189-119">The file is closed automatically after each logging operation.</span></span> <span data-ttu-id="24189-120">O mesmo arquivo de log é usado para entradas de aplicativo e de sistema.</span><span class="sxs-lookup"><span data-stu-id="24189-120">The same log file is used for application entries and system entries.</span></span>

<span data-ttu-id="24189-121">As etapas a seguir mostram como usar o objeto de log:</span><span class="sxs-lookup"><span data-stu-id="24189-121">The following steps show how to use the logging object:</span></span>

1.  <span data-ttu-id="24189-122">Inclua wmdmlog. h em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="24189-122">Include wmdmlog.h in your project.</span></span>
2.  <span data-ttu-id="24189-123">Crie um objeto de log chamando **CoCreateInstance**(CLSID \_ WMDMLogger) e solicitando a interface **IWMDMLogger** .</span><span class="sxs-lookup"><span data-stu-id="24189-123">Create a logging object by calling **CoCreateInstance**(CLSID\_WMDMLogger) and requesting the **IWMDMLogger** interface.</span></span> <span data-ttu-id="24189-124">Atribua o ponteiro de interface a uma variável global.</span><span class="sxs-lookup"><span data-stu-id="24189-124">Assign the interface pointer to a global variable.</span></span>
3.  <span data-ttu-id="24189-125">Verifique se o log está habilitado chamando [**IWMDMLogger:: IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); Se não estiver, habilite-a chamando [**IWMDMLogger:: Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span><span class="sxs-lookup"><span data-stu-id="24189-125">Verify that logging is enabled by calling [**IWMDMLogger::IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); if it is not, enable it by calling [**IWMDMLogger::Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span></span>
4.  <span data-ttu-id="24189-126">Especifique um nome e um tamanho de arquivo de log personalizados.</span><span class="sxs-lookup"><span data-stu-id="24189-126">Specify a custom log file name and size.</span></span> <span data-ttu-id="24189-127">Isso é feito chamando [**IWMDMLogger:: Setlogfilename**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) e [**IWMDMLogger:: SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).</span><span class="sxs-lookup"><span data-stu-id="24189-127">This is done by calling [**IWMDMLogger::SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) and [**IWMDMLogger::SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).</span></span>
5.  <span data-ttu-id="24189-128">Em pontos no código em que você deseja fazer uma entrada no log, chame [**IWMDMLogger:: LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) para cadeias de caracteres de log que contêm variáveis (esse método é semelhante a **wsprintf** da maneira que permite formatar uma cadeia de caracteres contendo um valor de variável) ou chamar [**IWMDMLogger:: LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) para registrar cadeias de caracteres constantes.</span><span class="sxs-lookup"><span data-stu-id="24189-128">At points in your code where you want to make an entry in the log, call either [**IWMDMLogger::LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) to log strings containing variables (this method is similar to **wsprintf** in the way it allows you to format a string containing a variable value), or call [**IWMDMLogger::LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) to log constant strings.</span></span>

<span data-ttu-id="24189-129">Para obter um exemplo de código, consulte as páginas de referência para os métodos de [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span><span class="sxs-lookup"><span data-stu-id="24189-129">For example code, see the reference pages for the methods of [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span>

## <a name="related-topics"></a><span data-ttu-id="24189-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24189-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24189-131">**Tarefas comuns a aplicativos e provedores de serviços**</span><span class="sxs-lookup"><span data-stu-id="24189-131">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




