---
description: 'Saiba mais sobre: Implementando um decodificador de WIC-Enabled'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implementando um decodificador de WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0aa2211c0b21e8f6fc921986406f7079b13c216f0bd7ada684e7748effb6c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205697"
---
# <a name="implementing-a-wic-enabled-decoder"></a>Implementando um decodificador de WIC-Enabled


a implementação de um decodificador de WIC (Windows Imaging Component) requer a gravação de duas classes. as interfaces nessas classes correspondem diretamente às responsabilidades do decodificador descritas na seção [decodificação](-wic-howwicworks.md) de [como funciona o componente de Windows Imaging](-wic-howwicworks.md).

Uma das classes fornece serviços de nível de contêiner e implementa a interface [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) . Se o formato de imagem der suporte a metadados em nível de contêiner, você também deverá implementar a interface [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) nessa classe. É recomendável que você dê suporte à interface [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) no decodificador e no codificador para dar suporte a uma melhor experiência do usuário.

A outra classe que você implementará fornece serviços de nível de quadro e fará a decodificação real dos bits de imagem para cada quadro no contêiner. Essa classe implementa a interface [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) e a interface [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) . Se você estiver escrevendo um decodificador para um formato bruto, também implementará a interface [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) nessa classe. Além das interfaces necessárias, é altamente recomendável que você implemente a interface [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) nessa classe para habilitar o melhor desempenho possível para seu formato de imagem.

Um dos objetos fornecidos pelo WIC é o [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory). Você usa frequentemente a interface [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) nesse objeto para criar vários componentes. Como ele é usado com frequência, você deve manter uma referência a ele como uma propriedade de membro nas classes do decodificador e do codificador.


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[como funciona o componente de Windows Imaging](-wic-howwicworks.md)
</dt> <dt>

[Interfaces do decodificador](-wic-decoderinterfaces.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de geração de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral dos metadados do WIC](-wic-about-metadata.md)
</dt> <dt>

[Visão geral da codificação](-wic-creating-encoder.md)
</dt> </dl>

 

 



