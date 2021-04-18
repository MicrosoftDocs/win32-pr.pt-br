---
title: Suporte a imagens personalizadas para dispositivos
description: Suporte a imagens personalizadas para dispositivos
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Windows Media Player, suporte a imagens personalizadas para dispositivos
- Windows Media Player, suporte a imagens para dispositivos
- suporte a imagens personalizadas do dispositivo
- suporte a imagens personalizadas para dispositivos
- suporte a imagens para dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105761473"
---
# <a name="custom-image-support-for-devices"></a><span data-ttu-id="d7152-108">Suporte a imagens personalizadas para dispositivos</span><span class="sxs-lookup"><span data-stu-id="d7152-108">Custom Image Support for Devices</span></span>

> [!Note]  
> <span data-ttu-id="d7152-109">Esta seção documenta um recurso do Windows Media Player 10 que está disponível ao usar o sistema operacional Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d7152-109">This section documents a feature of Windows Media Player 10 that is available when using the Windows XP operating system.</span></span> <span data-ttu-id="d7152-110">Ele pode não estar disponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d7152-110">It may be unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d7152-111">Os fabricantes de dispositivos podem fornecer dois arquivos de imagem especiais para personalizar a maneira como um dispositivo é representado na interface do usuário do Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="d7152-111">Device manufacturers can provide two special image files to customize the way a device is represented in the Windows Media Player 10 user interface.</span></span> <span data-ttu-id="d7152-112">Esses dois arquivos são:</span><span class="sxs-lookup"><span data-stu-id="d7152-112">These two files are:</span></span>

-   <span data-ttu-id="d7152-113">DevIcon. fil.</span><span class="sxs-lookup"><span data-stu-id="d7152-113">DevIcon.fil.</span></span> <span data-ttu-id="d7152-114">Um arquivo de formato de ícone do Windows que representa o hardware do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7152-114">A Windows icon format file that represents the device hardware.</span></span> <span data-ttu-id="d7152-115">Essa imagem é exibida no Windows Media Player 10 em qualquer lugar em que um ícone é usado para representar um dispositivo, como a lista de dispositivos no recurso de **sincronização** .</span><span class="sxs-lookup"><span data-stu-id="d7152-115">This image displays in Windows Media Player 10 anywhere an icon is used to represent a device, such as the device list in the **Sync** feature.</span></span>
-   <span data-ttu-id="d7152-116">Devlog. fil.</span><span class="sxs-lookup"><span data-stu-id="d7152-116">DevLogo.fil.</span></span> <span data-ttu-id="d7152-117">Um arquivo de formato PNG que representa o logotipo corporativo do fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7152-117">A PNG format file that represents the corporate logo of the device manufacturer.</span></span> <span data-ttu-id="d7152-118">Essa imagem é exibida no Windows Media Player 10 em qualquer lugar da identidade visual corporativa que é usada, como a caixa de diálogo **configuração do dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="d7152-118">This image displays in Windows Media Player 10 anywhere corporate branding is used, such as the **Device Setup** dialog box.</span></span>

## <a name="general-guidelines-for-images"></a><span data-ttu-id="d7152-119">Diretrizes gerais para imagens</span><span class="sxs-lookup"><span data-stu-id="d7152-119">General Guidelines for Images</span></span>

<span data-ttu-id="d7152-120">As diretrizes a seguir se aplicam ao suporte de imagem personalizada em geral:</span><span class="sxs-lookup"><span data-stu-id="d7152-120">The following guidelines apply to custom image support in general:</span></span>

-   <span data-ttu-id="d7152-121">Esse recurso é opcional.</span><span class="sxs-lookup"><span data-stu-id="d7152-121">This feature is optional.</span></span> <span data-ttu-id="d7152-122">Os dispositivos que não fornecem imagens serão representados por imagens padrão.</span><span class="sxs-lookup"><span data-stu-id="d7152-122">Devices that do not supply images will be represented by default images.</span></span>
-   <span data-ttu-id="d7152-123">Esse recurso tem suporte somente para dispositivos habilitados para MTP.</span><span class="sxs-lookup"><span data-stu-id="d7152-123">This feature is supported for MTP-enabled devices only.</span></span>
-   <span data-ttu-id="d7152-124">Para evitar alterações nos arquivos, é recomendável que os arquivos de imagem sejam armazenados no firmware ou em um meio de armazenamento protegido, não com arquivos criados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d7152-124">To prevent changes to the files, it is recommended that the image files be stored in firmware or a protected storage medium, not with user-created files.</span></span>
-   <span data-ttu-id="d7152-125">Os arquivos não devem ser retornados para os clientes do Windows Media Gerenciador de Dispositivos que enumeram o armazenamento raiz do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7152-125">The files should not be returned to Windows Media Device Manager clients that enumerate the root storage of the device.</span></span> <span data-ttu-id="d7152-126">Além disso, excluir, mover ou renomear os arquivos deve falhar.</span><span class="sxs-lookup"><span data-stu-id="d7152-126">Also, deleting, moving, or renaming the files should fail.</span></span>
-   <span data-ttu-id="d7152-127">Se o dispositivo fornecer mais de um meio de armazenamento, o dispositivo deverá retornar os arquivos de imagem em resposta às solicitações de abertura de arquivo de qualquer meio.</span><span class="sxs-lookup"><span data-stu-id="d7152-127">If the device provides more than one storage medium, the device should return the image files in response to file open requests from any medium.</span></span> <span data-ttu-id="d7152-128">Ícones de dispositivo diferentes podem ser retornados de cada meio de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d7152-128">Different device icons may be returned from each storage medium.</span></span>
-   <span data-ttu-id="d7152-129">Para clientes habilitados para Windows Media Gerenciador de Dispositivos 1,2, essas imagens terão precedência sobre as propriedades de ícone fornecidas pelos mecanismos de instalação do Windows, como propriedades do nó do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7152-129">For Windows Media Device Manager 1.2-enabled clients, these images will take precedence over icon properties supplied by Windows setup mechanisms, such as device node properties.</span></span>
-   <span data-ttu-id="d7152-130">As imagens não devem conter nenhuma informação que exija localização.</span><span class="sxs-lookup"><span data-stu-id="d7152-130">The images must not contain any information that requires localization.</span></span>
-   <span data-ttu-id="d7152-131">Para dispositivos com várias funções, somente os recursos de reprodução de música do Windows XP usarão essas imagens.</span><span class="sxs-lookup"><span data-stu-id="d7152-131">For multi-function devices, only the music playback features of Windows XP will use these images.</span></span>

## <a name="creating-the-device-icon-image"></a><span data-ttu-id="d7152-132">Criando a imagem de ícone do dispositivo</span><span class="sxs-lookup"><span data-stu-id="d7152-132">Creating the Device Icon Image</span></span>

<span data-ttu-id="d7152-133">O arquivo de imagem do ícone do dispositivo, DevIcon. Fil, deve conter um arquivo no formato de ícone do Windows.</span><span class="sxs-lookup"><span data-stu-id="d7152-133">The device icon image file, DevIcon.fil, must contain a file in Windows icon format.</span></span> <span data-ttu-id="d7152-134">Os ícones de artigo [do MSDN no Win32](/previous-versions/ms997538(v=msdn.10)) descrevem como criar um arquivo desse tipo.</span><span class="sxs-lookup"><span data-stu-id="d7152-134">The MSDN article [Icons in Win32](/previous-versions/ms997538(v=msdn.10)) describes how to create such a file.</span></span> <span data-ttu-id="d7152-135">O artigo do MSDN [criando ícones do Windows XP](/previous-versions/ms997636(v=msdn.10)) fornece diretrizes de estilo para ícones do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d7152-135">The MSDN article [Creating Windows XP Icons](/previous-versions/ms997636(v=msdn.10)) provides style guidelines for Windows XP icons.</span></span> <span data-ttu-id="d7152-136">O arquivo de imagem do ícone do dispositivo incorpora doze imagens em um único arquivo, fornecendo quatro tamanhos diferentes com três profundidades de cor diferentes cada.</span><span class="sxs-lookup"><span data-stu-id="d7152-136">The device icon image file incorporates twelve images in a single file by providing four different sizes with three different color depths each.</span></span>

<span data-ttu-id="d7152-137">Certifique-se de prestar atenção especial às seguintes diretrizes:</span><span class="sxs-lookup"><span data-stu-id="d7152-137">Be certain to pay particular attention to the following guidelines:</span></span>

-   <span data-ttu-id="d7152-138">Os tamanhos recomendados (em pixels) são 16x16, 32x32, 48x48 e 256x256.</span><span class="sxs-lookup"><span data-stu-id="d7152-138">Recommended sizes (in pixels) are 16x16, 32x32, 48x48, and 256x256.</span></span>
-   <span data-ttu-id="d7152-139">As profundidades de cor recomendadas são de 24 bits com canal alfa de 8 bits, 8 bits com transparência de 1 bit e 4 bits com transparência de 1 bit.</span><span class="sxs-lookup"><span data-stu-id="d7152-139">Recommended color depths are 24-bit with 8-bit alpha channel, 8-bit with 1-bit transparency, and 4-bit with 1-bit transparency.</span></span>
-   <span data-ttu-id="d7152-140">Use o ângulo de perspectiva e as recomendações de sombra descritas nos artigos do MSDN mencionados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d7152-140">Use the perspective angle and drop shadow recommendations described in the MSDN articles mentioned previously.</span></span>

<span data-ttu-id="d7152-141">Depois de criar o arquivo de ícone, basta renomeá-lo DevIcon. fil.</span><span class="sxs-lookup"><span data-stu-id="d7152-141">Once you have created the icon file, simply rename it DevIcon.fil.</span></span>

## <a name="creating-the-corporate-logo-image"></a><span data-ttu-id="d7152-142">Criando a imagem do logotipo corporativo</span><span class="sxs-lookup"><span data-stu-id="d7152-142">Creating the Corporate Logo Image</span></span>

<span data-ttu-id="d7152-143">O arquivo de imagem de logotipo corporativo, devlogo. Fil, deve conter um arquivo no formato PNG.</span><span class="sxs-lookup"><span data-stu-id="d7152-143">The corporate logo image file, DevLogo.fil, must contain a file in PNG format.</span></span> <span data-ttu-id="d7152-144">Use as seguintes diretrizes ao criar a imagem:</span><span class="sxs-lookup"><span data-stu-id="d7152-144">Use the following guidelines when creating the image:</span></span>

-   <span data-ttu-id="d7152-145">As dimensões máximas para a imagem são 150x32 pixels.</span><span class="sxs-lookup"><span data-stu-id="d7152-145">The maximum dimensions for the image are 150x32 pixels.</span></span>
-   <span data-ttu-id="d7152-146">A imagem deve dar suporte à mesclagem alfa para habilitar uma transição suave entre a interface do usuário do Windows Media Player 10 e o logotipo.</span><span class="sxs-lookup"><span data-stu-id="d7152-146">The image should support alpha blending to enable a smooth transition between the Windows Media Player 10 user interface and the logo.</span></span>

<span data-ttu-id="d7152-147">Depois de criar o arquivo de logotipo corporativo, basta renomeá-lo como desvlogo. fil.</span><span class="sxs-lookup"><span data-stu-id="d7152-147">Once you have created the corporate logo file, simply rename it DevLogo.fil.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7152-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7152-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7152-149">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="d7152-149">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 