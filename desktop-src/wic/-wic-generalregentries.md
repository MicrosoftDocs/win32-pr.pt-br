---
description: Entradas gerais do registro
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: Entradas gerais do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7c3514adcc0aeaaf9adadd2b71dfdffcd8d408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796211"
---
# <a name="general-registry-entries"></a><span data-ttu-id="bec5c-103">Entradas gerais do registro</span><span class="sxs-lookup"><span data-stu-id="bec5c-103">General Registry Entries</span></span>


<span data-ttu-id="bec5c-104">As seguintes entradas de registro devem ser feitas separadamente para o decodificador e o codificador:</span><span class="sxs-lookup"><span data-stu-id="bec5c-104">The following registry entries must be made separately for both the decoder and the encoder:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

<span data-ttu-id="bec5c-105">São necessárias as entradas amigável, VendorGUID, ContainerFormat, MimeTypes, sqlextensions e formats.</span><span class="sxs-lookup"><span data-stu-id="bec5c-105">The FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions, and Formats entries are required.</span></span> <span data-ttu-id="bec5c-106">Todos os outros são opcionais.</span><span class="sxs-lookup"><span data-stu-id="bec5c-106">All of the others are optional.</span></span>

<span data-ttu-id="bec5c-107">Observe que as entradas DeviceManufacturer e DeviceModels são específicas para codecs brutos e se referem ao fabricante da câmera e aos modelos de câmera aos quais o codec se aplica.</span><span class="sxs-lookup"><span data-stu-id="bec5c-107">Note that the DeviceManufacturer and DeviceModels entries are specific to raw codecs and refer to the camera manufacturer and camera models that the codec is applicable to.</span></span> <span data-ttu-id="bec5c-108">A versão de especificação é a versão da especificação de formato de imagem com a qual o codec está em conformidade.</span><span class="sxs-lookup"><span data-stu-id="bec5c-108">The spec version is the version of the image format specification with which the codec complies.</span></span> <span data-ttu-id="bec5c-109">A entrada de formatos especifica os formatos de pixel com suporte pelo codec.</span><span class="sxs-lookup"><span data-stu-id="bec5c-109">The Formats entry specifies the pixel formats supported by the codec.</span></span> <span data-ttu-id="bec5c-110">Um codec pode dar suporte a mais de um formato de pixel.</span><span class="sxs-lookup"><span data-stu-id="bec5c-110">A codec may support more than one pixel format.</span></span> <span data-ttu-id="bec5c-111">Nesse caso, você inseriria várias chaves em formatos HKEY \_ classes \_ raiz \\ CLSID \\ {Encoder/Decoder CLSID} \\ .</span><span class="sxs-lookup"><span data-stu-id="bec5c-111">In that case, you would enter multiple keys under HKEY\_CLASSES\_ROOT\\CLSID\\{Encoder/Decoder CLSID}\\Formats.</span></span>

## <a name="arbitrationpriority"></a><span data-ttu-id="bec5c-112">ArbitrationPriority</span><span class="sxs-lookup"><span data-stu-id="bec5c-112">ArbitrationPriority</span></span>

<span data-ttu-id="bec5c-113">A partir do Windows 8, o ArbitrationPriority é uma nova entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="bec5c-113">Starting in Windows 8, ArbitrationPriority is a new registry entry.</span></span> <span data-ttu-id="bec5c-114">Os valores válidos são 0 a 10.</span><span class="sxs-lookup"><span data-stu-id="bec5c-114">Valid values are 0 through 10.</span></span> <span data-ttu-id="bec5c-115">Quando a chave ArbitrationPriority estiver presente, o valor dessa chave instruirá o WIC a priorizar o codec associado por trás de qualquer outro codec com um valor de ArbitrationPriority inferior.</span><span class="sxs-lookup"><span data-stu-id="bec5c-115">When the ArbitrationPriority key is present, the value of this key will instruct WIC to prioritize the associated codec behind any other codecs with a lower ArbitrationPriority value.</span></span> <span data-ttu-id="bec5c-116">Essa avaliação ocorre antes que ocorra a arbitragem do codec do WIC existente e garante que o codec associado seja priorizado abaixo de qualquer codec concorrente, mesmo que seja o que for mais compatível.</span><span class="sxs-lookup"><span data-stu-id="bec5c-116">This evaluation occurs before the existing WIC codec arbitration occurs, and ensures the associated codec is prioritized below any competing codec, even if it is as or more capable.</span></span> <span data-ttu-id="bec5c-117">Qualquer codec que não tenha um valor ArbitrationPriority explícito definido no registro terá como padrão a prioridade 0.</span><span class="sxs-lookup"><span data-stu-id="bec5c-117">Any codec that doesn’t have an explicit ArbitrationPriority value defined in the registry will default to Priority 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bec5c-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bec5c-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bec5c-119">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="bec5c-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bec5c-120">Instalação e registro de CODEC</span><span class="sxs-lookup"><span data-stu-id="bec5c-120">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="bec5c-121">Entradas de registro específicas do codificador</span><span class="sxs-lookup"><span data-stu-id="bec5c-121">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="bec5c-122">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="bec5c-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="bec5c-123">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="bec5c-123">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="bec5c-124">**Como funciona o Windows Imaging Component: descoberta e arbitragem de codec**</span><span class="sxs-lookup"><span data-stu-id="bec5c-124">**How the Windows Imaging Component Works: Codec Discovery and Arbitration**</span></span>](-wic-howwicworks.md)
</dt> </dl>

 

 



