---
description: Este aplicativo de exemplo usa as APIs de áudio principais para alterar o volume do dispositivo, conforme especificado pelo usuário.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457067"
---
# <a name="endpointvolume"></a><span data-ttu-id="a6839-103">EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="a6839-103">EndpointVolume</span></span>

<span data-ttu-id="a6839-104">Este aplicativo de exemplo usa as APIs de áudio principais para alterar o volume do dispositivo, conforme especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a6839-104">This sample application uses the Core Audio APIs to change the volume of the device, as specified by the user.</span></span>

<span data-ttu-id="a6839-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="a6839-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a6839-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6839-106">Description</span></span>](#description)
-   [<span data-ttu-id="a6839-107">Requirements</span><span class="sxs-lookup"><span data-stu-id="a6839-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a6839-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a6839-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="a6839-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a6839-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="a6839-110">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a6839-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="a6839-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6839-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="a6839-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6839-112">Description</span></span>

<span data-ttu-id="a6839-113">Este exemplo demonstra os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a6839-113">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="a6839-114">[API MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.</span><span class="sxs-lookup"><span data-stu-id="a6839-114">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="a6839-115">[API EndpointVolume](endpointvolume-api.md) para controlar os níveis de volume do ponto de extremidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6839-115">[EndpointVolume API](endpointvolume-api.md) to control volume levels of the device endpoint.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6839-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6839-116">Requirements</span></span>



| <span data-ttu-id="a6839-117">Produto</span><span class="sxs-lookup"><span data-stu-id="a6839-117">Product</span></span>                                                        | <span data-ttu-id="a6839-118">Versão</span><span class="sxs-lookup"><span data-stu-id="a6839-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="a6839-119">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="a6839-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="a6839-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a6839-120">Windows 7</span></span> |
| <span data-ttu-id="a6839-121">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a6839-121">Visual Studio</span></span>                                                  | <span data-ttu-id="a6839-122">2008</span><span class="sxs-lookup"><span data-stu-id="a6839-122">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="a6839-123">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a6839-123">Downloading the Sample</span></span>

<span data-ttu-id="a6839-124">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="a6839-124">This sample is available in the following locations.</span></span>



| <span data-ttu-id="a6839-125">Local</span><span class="sxs-lookup"><span data-stu-id="a6839-125">Location</span></span>    | <span data-ttu-id="a6839-126">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="a6839-126">Path/URL</span></span>                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6839-127">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="a6839-127">Windows SDK</span></span> | <span data-ttu-id="a6839-128">\\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ EndpointVolume \\ ...</span><span class="sxs-lookup"><span data-stu-id="a6839-128">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\EndpointVolume\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="a6839-129">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a6839-129">Building the Sample</span></span>

<span data-ttu-id="a6839-130">Para criar o exemplo x, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="a6839-130">To build the x sample, use the following steps:</span></span>

<span data-ttu-id="a6839-131">Para criar o exemplo de EndpointVolumeChanger, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="a6839-131">To build the EndpointVolumeChanger sample, use the following steps:</span></span>

1.  <span data-ttu-id="a6839-132">Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="a6839-132">Open the CMD shell for the Windows SDK and change to the EndpointVolume sample directory.</span></span>
2.  <span data-ttu-id="a6839-133">Execute o comando `start EndpointVolumeChanger.sln` no diretório EndpointVolume para abrir o projeto EndpointVolumeChanger na janela do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a6839-133">Run the command `start EndpointVolumeChanger.sln` in the EndpointVolume directory to open the EndpointVolumeChanger project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="a6839-134">De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** .</span><span class="sxs-lookup"><span data-stu-id="a6839-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="a6839-135">Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK.</span><span class="sxs-lookup"><span data-stu-id="a6839-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="a6839-136">Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, WASAPIEndpointVolume. vcproj.</span><span class="sxs-lookup"><span data-stu-id="a6839-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIEndpointVolume.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a6839-137">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a6839-137">Running the Sample</span></span>

<span data-ttu-id="a6839-138">Se você criar o aplicativo de demonstração com êxito, um arquivo executável, EndpointVolumeChanger.exe, será gerado.</span><span class="sxs-lookup"><span data-stu-id="a6839-138">If you build the demo application successfully, an executable file, EndpointVolumeChanger.exe, is generated.</span></span> <span data-ttu-id="a6839-139">Para executá-lo, digite `EndpointVolumeChanger` uma janela de comando seguida por argumentos obrigatórios ou opcionais.</span><span class="sxs-lookup"><span data-stu-id="a6839-139">To run it, type `EndpointVolumeChanger` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="a6839-140">O exemplo a seguir mostra como alternar a configuração de mudo no dispositivo de console padrão.</span><span class="sxs-lookup"><span data-stu-id="a6839-140">The following example shows how to toggle the mute setting on the default console device.</span></span>

`EndpointVolumeChanger.exe -console -m`

<span data-ttu-id="a6839-141">A tabela a seguir mostra os argumentos.</span><span class="sxs-lookup"><span data-stu-id="a6839-141">The following table shows the arguments.</span></span>

| <span data-ttu-id="a6839-142">Argumento</span><span class="sxs-lookup"><span data-stu-id="a6839-142">Argument</span></span>        | <span data-ttu-id="a6839-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6839-143">Description</span></span>                                                         |
|-----------------|---------------------------------------------------------------------|
| <span data-ttu-id="a6839-144">-?</span><span class="sxs-lookup"><span data-stu-id="a6839-144">-?</span></span>              | <span data-ttu-id="a6839-145">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="a6839-145">Shows help.</span></span>                                                         |
| <span data-ttu-id="a6839-146">-H</span><span class="sxs-lookup"><span data-stu-id="a6839-146">-h</span></span>              | <span data-ttu-id="a6839-147">Mostra a ajuda.</span><span class="sxs-lookup"><span data-stu-id="a6839-147">Shows help.</span></span>                                                         |
| -+              | <span data-ttu-id="a6839-148">Incrementa o nível de volume no dispositivo de ponto de extremidade de áudio por uma etapa.</span><span class="sxs-lookup"><span data-stu-id="a6839-148">Increments the volume level on audio endpoint device by one step.</span></span> <span data-ttu-id="a6839-149">.</span><span class="sxs-lookup"><span data-stu-id="a6839-149">.</span></span> |
| <span data-ttu-id="a6839-150">-up</span><span class="sxs-lookup"><span data-stu-id="a6839-150">-up</span></span>             | <span data-ttu-id="a6839-151">Incrementa o nível de volume no dispositivo de ponto de extremidade de áudio por uma etapa.</span><span class="sxs-lookup"><span data-stu-id="a6839-151">Increments the volume level on audio endpoint device by one step.</span></span>   |
| --              | <span data-ttu-id="a6839-152">Decrementa o nível de volume no dispositivo de ponto de extremidade de áudio por uma etapa.</span><span class="sxs-lookup"><span data-stu-id="a6839-152">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="a6839-153">-para baixo</span><span class="sxs-lookup"><span data-stu-id="a6839-153">-down</span></span>           | <span data-ttu-id="a6839-154">Decrementa o nível de volume no dispositivo de ponto de extremidade de áudio por uma etapa.</span><span class="sxs-lookup"><span data-stu-id="a6839-154">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="a6839-155">-v</span><span class="sxs-lookup"><span data-stu-id="a6839-155">-v</span></span>              | <span data-ttu-id="a6839-156">Define o nível de volume mestre no dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="a6839-156">Sets the master volume level on the audio endpoint device.</span></span>          |
| <span data-ttu-id="a6839-157">-console</span><span class="sxs-lookup"><span data-stu-id="a6839-157">-console</span></span>        | <span data-ttu-id="a6839-158">Use o dispositivo de console padrão.</span><span class="sxs-lookup"><span data-stu-id="a6839-158">Use the default console device.</span></span>                                     |
| <span data-ttu-id="a6839-159">-comunicações</span><span class="sxs-lookup"><span data-stu-id="a6839-159">-communications</span></span> | <span data-ttu-id="a6839-160">Use o dispositivo de comunicação padrão.</span><span class="sxs-lookup"><span data-stu-id="a6839-160">Use the default communication device.</span></span>                               |
| <span data-ttu-id="a6839-161">-multimídia</span><span class="sxs-lookup"><span data-stu-id="a6839-161">-multimedia</span></span>     | <span data-ttu-id="a6839-162">Use o dispositivo multimídia padrão.</span><span class="sxs-lookup"><span data-stu-id="a6839-162">Use the default multimedia device.</span></span>                                  |
| <span data-ttu-id="a6839-163">-ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="a6839-163">-endpoint</span></span>       | <span data-ttu-id="a6839-164">Use o identificador de ponto de extremidade especificado no valor de opção.</span><span class="sxs-lookup"><span data-stu-id="a6839-164">Use the endpoint identifier specified in the switch value.</span></span>          |



 

<span data-ttu-id="a6839-165">Se o aplicativo for executado sem argumentos, ele enumerará os dispositivos disponíveis e solicitará que o usuário selecione um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6839-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device.</span></span> <span data-ttu-id="a6839-166">Depois que o usuário especifica o dispositivo, o aplicativo exibe as configurações de volume atuais para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a6839-166">After the user specifies the device, the application displays the current volume settings for the endpoint.</span></span> <span data-ttu-id="a6839-167">O volume pode ser controlado usando as opções descritas na tabela anterior.</span><span class="sxs-lookup"><span data-stu-id="a6839-167">The volume can be controlled by using the switches described in the preceding table.</span></span>

<span data-ttu-id="a6839-168">Para obter mais informações sobre como controlar os níveis de volume de dispositivos de ponto de extremidade de áudio, consulte [API do EndpointVolume](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="a6839-168">For more information about controlling the volume levels of audio endpoint devices, see [EndpointVolume API](endpointvolume-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6839-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6839-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6839-170">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="a6839-170">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



