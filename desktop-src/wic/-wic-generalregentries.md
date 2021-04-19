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
# <a name="general-registry-entries"></a>Entradas gerais do registro


As seguintes entradas de registro devem ser feitas separadamente para o decodificador e o codificador:

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

São necessárias as entradas amigável, VendorGUID, ContainerFormat, MimeTypes, sqlextensions e formats. Todos os outros são opcionais.

Observe que as entradas DeviceManufacturer e DeviceModels são específicas para codecs brutos e se referem ao fabricante da câmera e aos modelos de câmera aos quais o codec se aplica. A versão de especificação é a versão da especificação de formato de imagem com a qual o codec está em conformidade. A entrada de formatos especifica os formatos de pixel com suporte pelo codec. Um codec pode dar suporte a mais de um formato de pixel. Nesse caso, você inseriria várias chaves em formatos HKEY \_ classes \_ raiz \\ CLSID \\ {Encoder/Decoder CLSID} \\ .

## <a name="arbitrationpriority"></a>ArbitrationPriority

A partir do Windows 8, o ArbitrationPriority é uma nova entrada de registro. Os valores válidos são 0 a 10. Quando a chave ArbitrationPriority estiver presente, o valor dessa chave instruirá o WIC a priorizar o codec associado por trás de qualquer outro codec com um valor de ArbitrationPriority inferior. Essa avaliação ocorre antes que ocorra a arbitragem do codec do WIC existente e garante que o codec associado seja priorizado abaixo de qualquer codec concorrente, mesmo que seja o que for mais compatível. Qualquer codec que não tenha um valor ArbitrationPriority explícito definido no registro terá como padrão a prioridade 0.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Instalação e registro de CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Entradas de registro específicas do codificador](-wic-encoderregentries.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[**Como funciona o Windows Imaging Component: descoberta e arbitragem de codec**](-wic-howwicworks.md)
</dt> </dl>

 

 



