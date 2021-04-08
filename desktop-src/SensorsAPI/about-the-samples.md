---
description: O SDK do Windows inclui exemplos de código e ferramentas úteis para ajudá-lo a entender e usar o sensor do Windows e a plataforma de localização e APIs relacionadas.
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: Sobre os exemplos e ferramentas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126ec5e07829cfd17c2b07313bb104140c6fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829639"
---
# <a name="about-the-samples-and-tools"></a><span data-ttu-id="77af8-103">Sobre os exemplos e ferramentas</span><span class="sxs-lookup"><span data-stu-id="77af8-103">About the Samples and Tools</span></span>

<span data-ttu-id="77af8-104">O SDK do Windows inclui exemplos de código e ferramentas úteis para ajudá-lo a entender e usar o sensor do Windows e a plataforma de localização e APIs relacionadas.</span><span class="sxs-lookup"><span data-stu-id="77af8-104">The Windows SDK includes useful code samples and tools to help you understand and use the Windows Sensor and Location platform and related APIs.</span></span>

## <a name="samples"></a><span data-ttu-id="77af8-105">Exemplos</span><span class="sxs-lookup"><span data-stu-id="77af8-105">Samples</span></span>

<span data-ttu-id="77af8-106">O SDK do Windows inclui os exemplos de API do sensor a seguir.</span><span class="sxs-lookup"><span data-stu-id="77af8-106">The Windows SDK includes the following Sensor API samples.</span></span> <span data-ttu-id="77af8-107">Você pode encontrar os exemplos de API do sensor na pasta denominada \\ Samples \\ WinUI \\ sensores, em que você instalou o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="77af8-107">You can find the Sensor API samples in the folder named \\Samples\\winui\\Sensors, where you installed the Windows SDK.</span></span> <span data-ttu-id="77af8-108">Por exemplo, se você instalou o SDK do Windows na unidade C, encontraria os exemplos na seguinte pasta: C: Arquivos de \\ programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ WinUI \\ sensores.</span><span class="sxs-lookup"><span data-stu-id="77af8-108">For example, if you installed the Windows SDK on drive C, you would find the samples in the following folder: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\winui\\Sensors.</span></span>



| <span data-ttu-id="77af8-109">Nome da amostra</span><span class="sxs-lookup"><span data-stu-id="77af8-109">Sample name</span></span>       | <span data-ttu-id="77af8-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="77af8-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77af8-111">AmbientLightAware</span><span class="sxs-lookup"><span data-stu-id="77af8-111">AmbientLightAware</span></span> | <span data-ttu-id="77af8-112">Este exemplo de MFC mostra como usar a API do sensor lendo dados de sensores de luz ambiente no computador e alterando o tamanho do texto de acordo com as condições de iluminação.</span><span class="sxs-lookup"><span data-stu-id="77af8-112">This MFC sample shows how to use the Sensor API by reading data from ambient light sensors on the computer and changing text size according to the lighting conditions.</span></span> <span data-ttu-id="77af8-113">Você pode ver o código que mostra como gerenciar eventos e como solicitar permissões de usuário.</span><span class="sxs-lookup"><span data-stu-id="77af8-113">You can see code that shows how to manage events and how to request user permissions.</span></span> <span data-ttu-id="77af8-114">Você também pode ver um exemplo de como gerenciar a interface do usuário com base em condições de iluminação variáveis.</span><span class="sxs-lookup"><span data-stu-id="77af8-114">You can also see an example of how to manage the user interface based on varying lighting conditions.</span></span> <span data-ttu-id="77af8-115">Para obter mais informações, consulte [criando Light-Aware interfaces do usuário](creating-light-aware-user-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="77af8-115">For more information, see [Creating Light-Aware User Interfaces](creating-light-aware-user-interfaces.md).</span></span><br/> <span data-ttu-id="77af8-116">Você deve ter o Visual Studio 2008 instalado para criar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="77af8-116">You must have Visual Studio 2008 installed to build this sample.</span></span><br/> |



 

<span data-ttu-id="77af8-117">Para obter mais informações, consulte o arquivo chamado ReadMe.txt que está incluído no exemplo.</span><span class="sxs-lookup"><span data-stu-id="77af8-117">For more information, see the file named ReadMe.txt that is included with the sample.</span></span>

<span data-ttu-id="77af8-118">Você também pode baixar o exemplo de AmbientLightAware da Galeria de códigos.</span><span class="sxs-lookup"><span data-stu-id="77af8-118">You can also download the AmbientLightAware sample from Code Gallery.</span></span> <span data-ttu-id="77af8-119">Para obter mais informações, consulte a página de download com [reconhecimento de luz ambiente](/samples/browse/?redirectedfrom=MSDN-samples) .</span><span class="sxs-lookup"><span data-stu-id="77af8-119">For more information, see the [Ambient Light Aware](/samples/browse/?redirectedfrom=MSDN-samples) download page.</span></span>

## <a name="tools"></a><span data-ttu-id="77af8-120">Ferramentas</span><span class="sxs-lookup"><span data-stu-id="77af8-120">Tools</span></span>

<span data-ttu-id="77af8-121">O SDK do Windows inclui um sensor de luz virtual que você pode usar para simular um dispositivo de sensor de luz baseado em hardware.</span><span class="sxs-lookup"><span data-stu-id="77af8-121">The Windows SDK includes a virtual light sensor that you can use to simulate a hardware-based light sensor device.</span></span> <span data-ttu-id="77af8-122">Você pode usar essa ferramenta para fornecer dados para o exemplo de AmbientLightAware para ver como o código no exemplo funciona.</span><span class="sxs-lookup"><span data-stu-id="77af8-122">You can use this tool to provide data to the AmbientLightAware sample to see how the code in the sample works.</span></span>

<span data-ttu-id="77af8-123">A tabela a seguir descreve os arquivos que você deve usar para executar o sensor de luz virtual.</span><span class="sxs-lookup"><span data-stu-id="77af8-123">The following table describes the files you must use to run the virtual light sensor.</span></span> <span data-ttu-id="77af8-124">Você pode encontrar esses arquivos na pasta denominada bin, em que você instalou o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="77af8-124">You can find these files in the folder named Bin, where you installed the Windows SDK.</span></span> <span data-ttu-id="77af8-125">Por exemplo, se você instalou o SDK do Windows na unidade C em um computador de 32 bits, encontrará os arquivos do sensor de luz virtual na seguinte pasta: C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ bin.</span><span class="sxs-lookup"><span data-stu-id="77af8-125">For example, if you installed the Windows SDK on drive C on a 32-bit computer, you would find the virtual light sensor files in the following folder: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Bin.</span></span> <span data-ttu-id="77af8-126">Em computadores de 64 bits, você deve usar a versão de 64 bits da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="77af8-126">On 64-bit computers, you must use the 64-bit version of the tool.</span></span> <span data-ttu-id="77af8-127">No SDK do Windows, as ferramentas de 64 bits estão localizadas na subpasta chamada x64.</span><span class="sxs-lookup"><span data-stu-id="77af8-127">In the Windows SDK, 64-bit tools are located in the subfolder named x64.</span></span>



| <span data-ttu-id="77af8-128">Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="77af8-128">File name</span></span>                    | <span data-ttu-id="77af8-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="77af8-129">Description</span></span>                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77af8-130">VirtualLightSensor.exe</span><span class="sxs-lookup"><span data-stu-id="77af8-130">VirtualLightSensor.exe</span></span>       | <span data-ttu-id="77af8-131">Este programa fornece um controle deslizante que permite alterar o nível dos dados leves que o sensor virtual relata.</span><span class="sxs-lookup"><span data-stu-id="77af8-131">This program provides a slider control that enables you to change the level of the light data that the virtual sensor reports.</span></span> |
| <span data-ttu-id="77af8-132">VirtualLightSensorDriver.dll</span><span class="sxs-lookup"><span data-stu-id="77af8-132">VirtualLightSensorDriver.dll</span></span> | <span data-ttu-id="77af8-133">O driver de sensor lógico que simula um sensor de luz.</span><span class="sxs-lookup"><span data-stu-id="77af8-133">The logical sensor driver that simulates a light sensor.</span></span>                                                                       |
| <span data-ttu-id="77af8-134">VirtualLightSensorDriver. inf</span><span class="sxs-lookup"><span data-stu-id="77af8-134">VirtualLightSensorDriver.inf</span></span> | <span data-ttu-id="77af8-135">O arquivo INF do driver do sensor de luz virtual.</span><span class="sxs-lookup"><span data-stu-id="77af8-135">The INF file for the virtual light sensor driver.</span></span>                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a><span data-ttu-id="77af8-136">Instalando o sensor de luz virtual</span><span class="sxs-lookup"><span data-stu-id="77af8-136">Installing the Virtual Light Sensor</span></span>

<span data-ttu-id="77af8-137">Antes de usar o aplicativo sensor de luz virtual, você deve instalar o driver do sensor lógico.</span><span class="sxs-lookup"><span data-stu-id="77af8-137">Before you use the virtual light sensor application, you must install the logical sensor driver.</span></span> <span data-ttu-id="77af8-138">Siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="77af8-138">Follow these steps:</span></span>

1.  <span data-ttu-id="77af8-139">Abra uma janela de comando como administrador.</span><span class="sxs-lookup"><span data-stu-id="77af8-139">Open a command window as an administrator.</span></span>
2.  <span data-ttu-id="77af8-140">Altere para a pasta bin SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="77af8-140">Change to the Windows SDK Bin folder.</span></span>
3.  <span data-ttu-id="77af8-141">Digite **PnPUtil-a VirtualLightSensorDriver. inf**.</span><span class="sxs-lookup"><span data-stu-id="77af8-141">Type **pnputil -a VirtualLightSensorDriver.inf**.</span></span>
4.  <span data-ttu-id="77af8-142">Quando solicitado, clique em **instalar este driver de software mesmo assim**.</span><span class="sxs-lookup"><span data-stu-id="77af8-142">When prompted, click **Install this driver software anyway**.</span></span>
5.  <span data-ttu-id="77af8-143">Aguarde até que a janela de comando relate que o driver foi instalado com êxito.</span><span class="sxs-lookup"><span data-stu-id="77af8-143">Wait for the command window to report that the driver was successfully installed.</span></span>

### <a name="running-the-virtual-light-sensor"></a><span data-ttu-id="77af8-144">Executando o sensor de luz virtual</span><span class="sxs-lookup"><span data-stu-id="77af8-144">Running the Virtual Light Sensor</span></span>

<span data-ttu-id="77af8-145">Para executar o sensor de luz virtual, basta clicar duas vezes no arquivo. exe.</span><span class="sxs-lookup"><span data-stu-id="77af8-145">To run the virtual light sensor, simply double-click the .exe file.</span></span> <span data-ttu-id="77af8-146">Certifique-se de habilitar o sensor, quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="77af8-146">Be sure to enable the sensor, when prompted.</span></span>

<span data-ttu-id="77af8-147">Ao executar o programa, você pode observar que há um atraso antes que o sensor fique disponível.</span><span class="sxs-lookup"><span data-stu-id="77af8-147">When you run the program, you may notice that there is a delay before the sensor becomes available.</span></span> <span data-ttu-id="77af8-148">A interface do usuário do sensor de luz virtual exibirá a mensagem "aguardando" na barra de título enquanto o Gerenciador de sensor lógico criará um nó de dispositivo para o sensor lógico.</span><span class="sxs-lookup"><span data-stu-id="77af8-148">The virtual light sensor user interface will display the message "Waiting" in the title bar while the logical sensor manager creates a device node for the logical sensor.</span></span> <span data-ttu-id="77af8-149">Depois que a mensagem em espera desaparecer, você poderá usar o controle deslizante para definir o nível de saída Lux para o sensor de luz virtual.</span><span class="sxs-lookup"><span data-stu-id="77af8-149">After the waiting message goes away, you can use the slider to set the lux output level for the virtual light sensor.</span></span>

<span data-ttu-id="77af8-150">A imagem a seguir mostra a interface do usuário do sensor de luz virtual em seu estado pronto.</span><span class="sxs-lookup"><span data-stu-id="77af8-150">The following image shows the virtual light sensor user interface in its ready state.</span></span>

![interface do usuário do sensor de luz virtual](images/virtuallightsensor.png)

## <a name="related-topics"></a><span data-ttu-id="77af8-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77af8-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77af8-153">Sobre sensores lógicos</span><span class="sxs-lookup"><span data-stu-id="77af8-153">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> <dt>

[<span data-ttu-id="77af8-154">**\_luz da categoria do sensor \_**</span><span class="sxs-lookup"><span data-stu-id="77af8-154">**SENSOR\_CATEGORY\_LIGHT**</span></span>](sensor-category-light.md)
</dt> </dl>

 

