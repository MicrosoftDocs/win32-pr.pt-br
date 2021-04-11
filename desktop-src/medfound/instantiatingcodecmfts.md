---
description: Criando uma instância do codec MFTs
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Criando uma instância do codec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa886f24f7dbd1acc373c7e505baddf71bc3aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164572"
---
# <a name="instantiating-codec-mfts"></a>Criando uma instância do codec MFTs

[Media Foundation transformações](media-foundation-transforms.md) (MFTs) são objetos com que implementam a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . Um MFT é um objeto para transformar dados de multimídia como parte de um pipeline. Um pipeline é um grafo acíclico direcionado, que consiste em fontes de mídia, transformações de mídia e coletores de mídia. Um pipeline processa o streaming de dados de multimídia de forma assíncrona.

Embora MFTs possa ser instanciado e usado independentemente da infraestrutura de pipeline Media Foundation, é preferível usar a estrutura MediaFoundation sempre que possível.

Você pode criar um MFT de codec chamando a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . Você deve passar o identificador de classe do MFT, o identificador de interface de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)e um ponteiro para um ponteiro **IMFTransform** .

Os identificadores de classe do codec MFTs são definidos como constantes no arquivo de cabeçalho wmcodecdsp. h.

A constante para o identificador de interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) é \_ IMFTransform de IID.

O exemplo de código a seguir demonstra como criar uma instância de um MFT do Codec:


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 
