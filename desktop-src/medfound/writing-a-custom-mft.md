---
description: Esta seção descreve como escrever uma MFT (transformação Media Foundation) personalizada.
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Escrevendo um MFT personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c113867c719fc9c8512b5b0e1172ee0694e3905
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471652"
---
# <a name="writing-a-custom-mft"></a>Escrevendo um MFT personalizado

Esta seção descreve como escrever uma MFT (transformação Media Foundation) personalizada.

## <a name="mft-checklist"></a>Lista de verificação do MFT

Ao implementar um MFT personalizado, use a seguinte lista de verificação para determinar os requisitos:




| | | Todos os MFTs | Todos os MFTs devem implementar <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform.</strong></a><br /> Os tópicos a seguir dão mais informações sobre como implementar essa interface:<ul><li><a href="basic-mft-processing-model.md">Modelo básico de processamento MFT</a></li><li><a href="time-stamps-and-durations.md">Carimbos de data/hora e durações</a></li><li><a href="handling-stream-changes.md">Manipulando alterações de fluxo</a></li></ul><br /> | | Codificadores e decodificadores | Requisitos: <a href="implementing-a-codec-mft.md">consulte Implementando um Codec MFT</a>.<br /> Recomendado: <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>implemente IMFQualityAdvise</strong></a> <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>ou IMFQualityAdvise2</strong></a>para dar suporte a notificações de QoS (qualidade de serviço).<br /> | | Processadores de vídeo e decodificadores de vídeo | Opcional: suporte à aceleração de vídeo do DirectX.<br /><ul><li><a href="direct3d-aware-mfts.md">MFTs com conhecimento do Direct3D</a></li><li><a href="supporting-dxva-2-0-in-media-foundation.md">Suporte ao DXVA 2.0 no Media Foundation</a></li></ul> | | Codecs de hardware | Consulte <a href="hardware-mfts.md">Hardware MFTs</a>. | | Para tornar seu MFT descobrivel por aplicativos... | Consulte <a href="registering-and-enumerating-mfts.md">Registrando e enumerando MFTs</a>. | | Processamento de dados assíncrono | O modelo MFT padrão usa chamadas síncronas (bloqueio) para processar dados. Para alguns MFTs, o processamento assíncrono pode ser mais eficiente. No entanto, também é mais complexo implementar.<br /> Para obter mais informações, consulte <a href="asynchronous-mfts.md">MFTs assíncronos.</a><br /> | | Controle de taxa, modo de truque ou reprodução inversa | Consulte <a href="implementing-rate-control.md">Implementando o controle de taxa</a>. | | Se o MFT criar threads... | Implemente a interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient.</strong></a> | | Se o MFT tiver restrições de licenciamento... | Considere o uso do mecanismo de campo de uso. Consulte <a href="field-of-use-restrictions.md">Restrições de campo de uso.</a> | | Se você estiver portando um objeto de mídia DirectX existente (DMO)... | Consulte <a href="comparison-of-mfts-and-dmos.md">Comparação de MFTs e DMOs</a>. | 




 

Esta seção contém os seguintes tópicos:

-   [Carimbos de data/hora e durações](time-stamps-and-durations.md)
-   [Manipulando alterações de fluxo](handling-stream-changes.md)
-   [Implementando um Codec MFT](implementing-a-codec-mft.md)
-   [MFTs com conhecimento do Direct3D](direct3d-aware-mfts.md)
-   [Hardware MFTs](hardware-mfts.md)
-   [Codec Merit](codec-merit.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Media Foundation transformação](media-foundation-transforms.md)
</dt> </dl>

 

 




