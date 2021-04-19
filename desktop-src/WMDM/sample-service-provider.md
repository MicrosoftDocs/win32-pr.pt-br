---
title: Provedor de serviços de exemplo
description: Provedor de serviços de exemplo
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Gerenciador de Dispositivos de mídia do Windows, amostras
- Gerenciador de Dispositivos, exemplos
- Windows Media Gerenciador de Dispositivos, exemplo de provedor de serviço
- Gerenciador de Dispositivos, exemplo de provedor de serviço
- provedores de serviços, exemplos
- exemplos, provedores de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105800180"
---
# <a name="sample-service-provider"></a><span data-ttu-id="11f62-109">Provedor de serviços de exemplo</span><span class="sxs-lookup"><span data-stu-id="11f62-109">Sample Service Provider</span></span>

<span data-ttu-id="11f62-110">O SDK do Windows Media Gerenciador de Dispositivos inclui um provedor de serviços de exemplo para você usar.</span><span class="sxs-lookup"><span data-stu-id="11f62-110">The Windows Media Device Manager SDK includes a sample service provider for you to use.</span></span> <span data-ttu-id="11f62-111">Esse provedor de serviços inclui uma classe que relata cada disco rígido no computador como se ele fosse um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="11f62-111">This service provider includes a class that reports each hard drive on the computer as if it were an attached device.</span></span> <span data-ttu-id="11f62-112">O único aplicativo que usará esse provedor de serviços é o aplicativo de exemplo; O Windows Explorer não verá os "dispositivos" relatados por este provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="11f62-112">The only application that will use this service provider is the sample application; Windows Explorer will not see the "devices" reported by this service provider.</span></span> <span data-ttu-id="11f62-113">O exemplo de provedor de serviço é um objeto COM criado na ATL.</span><span class="sxs-lookup"><span data-stu-id="11f62-113">The service provider sample is a COM object built on ATL.</span></span> <span data-ttu-id="11f62-114">As etapas a seguir explicam como usar o provedor de serviços de exemplo:</span><span class="sxs-lookup"><span data-stu-id="11f62-114">The following steps explain how to use the sample service provider:</span></span>

> [!Note]  
> <span data-ttu-id="11f62-115">O provedor de serviços de exemplo implementa muito poucos recursos e, portanto, não deve ser usado para testar aplicativos do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="11f62-115">The sample service provider implements very few features, and so it should not be used for testing Windows Media Device Manager applications.</span></span> <span data-ttu-id="11f62-116">Para testar um aplicativo, use um provedor de serviços totalmente implementado.</span><span class="sxs-lookup"><span data-stu-id="11f62-116">To test an application, use a fully-implemented service provider.</span></span>

 

-   <span data-ttu-id="11f62-117">O exemplo foi enviado com um erro de codificação que fará com que o provedor de serviços não funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="11f62-117">The sample was shipped with a coding error that will cause the service provider to malfunction.</span></span> <span data-ttu-id="11f62-118">Para corrigir esse erro, abra o arquivo MDSPEnumStorage. cpp instalado na pasta < *caminho de instalação do SDK*  > \\ WMFSDK95 \\ WMDM \\ MDSP \\ mshdsp, vá para a linha 185 e altere a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="11f62-118">To correct this error, open the MDSPEnumStorage.cpp file installed in the folder < *SDK installation path* >\\WMFSDK95\\WMDM\\mdsp\\mshdsp, go to line 185, and change the following line:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

<span data-ttu-id="11f62-119">Para isso:</span><span class="sxs-lookup"><span data-stu-id="11f62-119">To this:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  <span data-ttu-id="11f62-120">Compile o arquivo de MsHDSP.dll.</span><span class="sxs-lookup"><span data-stu-id="11f62-120">Compile the MsHDSP.dll file.</span></span> <span data-ttu-id="11f62-121">Você pode fazer isso usando o NMAKE ou o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="11f62-121">You can do this using either NMAKE or Visual Studio.</span></span> <span data-ttu-id="11f62-122">Consulte [compilando o provedor de serviços de exemplo usando o NMAKE](compiling-the-sample-service-provider-using-nmake.md) ou [compilando o provedor de serviços de exemplo usando o Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) para saber como compilar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11f62-122">See [Compiling the Sample Service Provider Using NMAKE](compiling-the-sample-service-provider-using-nmake.md) or [Compiling the Sample Service Provider Using Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) to learn how to compile the application.</span></span>
2.  <span data-ttu-id="11f62-123">Registre MsHDSP.dll usando regsvr32.</span><span class="sxs-lookup"><span data-stu-id="11f62-123">Register MsHDSP.dll using regsvr32.</span></span> <span data-ttu-id="11f62-124">A linha a seguir, digitada em uma janela de prompt de comando na mesma pasta que MsHDSP.dll, registrará o provedor de serviços de exemplo:</span><span class="sxs-lookup"><span data-stu-id="11f62-124">The following line, typed into a command-prompt window in the same folder as MsHDSP.dll, will register the sample service provider:</span></span>

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    <span data-ttu-id="11f62-125">Para parar de representar um dispositivo, insira a seguinte linha no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="11f62-125">To stop impersonating a device, enter the following line at the command prompt:</span></span>

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  <span data-ttu-id="11f62-126">Os dispositivos removíveis representados por essa DLL só podem ser vistos pelo aplicativo de exemplo fornecido com esse SDK.</span><span class="sxs-lookup"><span data-stu-id="11f62-126">The removable devices impersonated by this DLL can only be seen by the sample application shipped with this SDK.</span></span> <span data-ttu-id="11f62-127">Compile o aplicativo de exemplo usando um dos métodos descritos em [aplicativo de desktop de exemplo](sample-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="11f62-127">Compile the sample application using one of the methods described in [Sample Desktop Application](sample-desktop-application.md).</span></span>
4.  <span data-ttu-id="11f62-128">Para depurar o provedor de serviços com o Visual Studio, abra o provedor de serviços no Visual Studio e selecione **Iniciar** no menu **depurar** .</span><span class="sxs-lookup"><span data-stu-id="11f62-128">To debug the service provider with Visual Studio, open the service provider in Visual Studio and select **Start** on the **Debug** menu.</span></span> <span data-ttu-id="11f62-129">Na caixa de diálogo pop-up, navegue até o aplicativo de exemplo que você criou na etapa anterior e clique em **OK**, e o provedor de serviços começará a ser executado no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="11f62-129">In the popup dialog box, browse to the sample application you built in the preceding step, and click **OK**, and the service provider will begin running in debug mode.</span></span>

    <span data-ttu-id="11f62-130">Para executar o provedor de serviços sem depuração no Visual Studio, basta registrar o msdhsp.dll e executar o aplicativo de desktop de exemplo que acompanha o SDK.</span><span class="sxs-lookup"><span data-stu-id="11f62-130">To run the service provider without debugging in Visual Studio, simply register the msdhsp.dll and run the sample desktop application that ships with the SDK.</span></span> <span data-ttu-id="11f62-131">O aplicativo de desktop de exemplo executa o provedor de serviços de exemplo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="11f62-131">The sample desktop application runs the sample service provider automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11f62-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11f62-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11f62-133">**Exemplos**</span><span class="sxs-lookup"><span data-stu-id="11f62-133">**Samples**</span></span>](samples.md)
</dt> </dl>

 

 




