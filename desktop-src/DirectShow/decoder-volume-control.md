---
description: Controle de volume do decodificador
ms.assetid: 94d68722-a0c2-47a7-a0a0-ae315f8f31ed
title: Controle de volume do decodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ce525f8b39e873d2c0002ac283014a9bcbe87c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370306"
---
# <a name="decoder-volume-control"></a><span data-ttu-id="d8a18-103">Controle de volume do decodificador</span><span class="sxs-lookup"><span data-stu-id="d8a18-103">Decoder Volume Control</span></span>

<span data-ttu-id="d8a18-104">Os aplicativos controlam o volume de áudio por meio da interface [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) .</span><span class="sxs-lookup"><span data-stu-id="d8a18-104">Applications control audio volume through the [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) interface.</span></span> <span data-ttu-id="d8a18-105">Um manipulador de interface **IBasicAudio** é fornecido para ksproxy.</span><span class="sxs-lookup"><span data-stu-id="d8a18-105">An **IBasicAudio** interface handler is provided for KSProxy.</span></span> <span data-ttu-id="d8a18-106">Para que um decodificador manipule os comandos de volume do KSProxy, ele deve adicionar várias chaves do registro em seu script de instalação e dar suporte ao conjunto de propriedades de **\_ onda KSPROPSETID** .</span><span class="sxs-lookup"><span data-stu-id="d8a18-106">For a decoder to handle the volume commands from KSProxy, it must add several registry keys in its setup script and support the **KSPROPSETID\_Wave** property set.</span></span>

<span data-ttu-id="d8a18-107">Crie algumas novas chaves do registro para o driver:</span><span class="sxs-lookup"><span data-stu-id="d8a18-107">Create some new registry keys for the driver:</span></span>


```C++
HKLM\SYSTEM\
  CurrentControlSet\Control
    DeviceClasses
      (decoder guid, eg 2721AE....)
        (Pnp id, eg ##?#VDGENDEV#...)
          #GLOBAL
            Device Parameters
              CLSID      REG_SZ   {17CCA...}
                FriendlyName   REG_SZ   WDM DVD Driver
                  Interfaces <--- create this key
                  {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
    MediaInterfaces
      {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
        (default)  REG_SZ   'KsProxy IBasicAudio handler' // Set this value.
        IID        REG_SZ   56 a8 68 b3 0a d4 11 ce b0 3a 00 20 af 0b a7 70 
                            // Create this key.
```



<span data-ttu-id="d8a18-108">Para implementar o controle de volume, o driver também deve dar suporte ao **KSPROPSETID \_ Wave**, juntamente com o volume Wave KsProperty.ID = KsProperty \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d8a18-108">To implement volume control, the driver also must support **KSPROPSETID\_Wave**, along with KsProperty.Id = KSPROPERTY\_WAVE\_VOLUME.</span></span> <span data-ttu-id="d8a18-109">Essa propriedade é passada para o driver por meio dos métodos [**IKsPropertySet:: Get**](ikspropertyset-get.md) e [**IKsPropertySet:: Set**](ikspropertyset-set.md) .</span><span class="sxs-lookup"><span data-stu-id="d8a18-109">This property is passed to the driver through the [**IKsPropertySet::Get**](ikspropertyset-get.md) and [**IKsPropertySet::Set**](ikspropertyset-set.md) methods.</span></span> <span data-ttu-id="d8a18-110">Os campos LeftAttenuation e RightAttentuation especificam os volumes do alto-falante esquerdo/direito como valores lineares de 0x0000 para 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="d8a18-110">The LeftAttenuation and RightAttentuation fields specify the left/right speaker volumes as linear values from 0x0000 to 0xffff.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8a18-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8a18-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8a18-112">Interfaces e especificações do decodificador</span><span class="sxs-lookup"><span data-stu-id="d8a18-112">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



