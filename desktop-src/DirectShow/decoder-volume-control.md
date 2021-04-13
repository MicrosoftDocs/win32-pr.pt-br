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
# <a name="decoder-volume-control"></a>Controle de volume do decodificador

Os aplicativos controlam o volume de áudio por meio da interface [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) . Um manipulador de interface **IBasicAudio** é fornecido para ksproxy. Para que um decodificador manipule os comandos de volume do KSProxy, ele deve adicionar várias chaves do registro em seu script de instalação e dar suporte ao conjunto de propriedades de **\_ onda KSPROPSETID** .

Crie algumas novas chaves do registro para o driver:


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



Para implementar o controle de volume, o driver também deve dar suporte ao **KSPROPSETID \_ Wave**, juntamente com o volume Wave KsProperty.ID = KsProperty \_ \_ . Essa propriedade é passada para o driver por meio dos métodos [**IKsPropertySet:: Get**](ikspropertyset-get.md) e [**IKsPropertySet:: Set**](ikspropertyset-set.md) . Os campos LeftAttenuation e RightAttentuation especificam os volumes do alto-falante esquerdo/direito como valores lineares de 0x0000 para 0xFFFF.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces e especificações do decodificador](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



