---
description: Diretrizes de implementação para serializar IWICDevelopRaw Configurações
ms.assetid: 4ecff5cc-24f3-4b89-b681-85c867b053e7
title: Diretrizes de implementação para serializar IWICDevelopRaw Configurações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119b6377fc8b75aa9763e8141e17ef79832a2aef5f010c2783a412cef0133788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709826"
---
# <a name="implementation-guidelines-for-serializing-iwicdevelopraw-settings"></a>Diretrizes de implementação para serializar IWICDevelopRaw Configurações

A interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expõe as configurações que o aplicativo pode usar para modificar o processamento da imagem RAW. As configurações devem ser capazes de ser serializadas para que elas persistam entre as sessões. Embora isso possa ser feito de várias maneiras, é recomendável codificar esses dados de maneira consistente com outros metadados.

Veja a seguir algumas diretrizes gerais de implementação:

-   As configurações feitas por meio de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) (como rotação ou saldo em branco) devem evitar a substituição da configuração da câmera ou dados "como disparo", a menos que a marca seja normalmente usada como uma "configuração atual". Por exemplo, marcas de orientação EXIF podem ser usadas para manter a rotação.
-   É preferível não ter que salvar todo o arquivo (incluindo os dados de pixel do mosaico) sempre que as configurações [**de IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) são solicitados a serem serializadas.
-   O processo de serialização das [**configurações de IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) geralmente seguirá essa ordem de eventos. O aplicativo:

    1.  Instalita um [**IWICBitmapDecoder em**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) um arquivo RAW.
    2.  Chama [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) para obter [**um IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) para o quadro RAW.
    3.  Chama QueryInterface na interface IWICBitmapFrameDecode para a interface IWICDevelopRaw.
    4.  Chama [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), que retorna uma interface IPropertyBag2 com todas as propriedades atuais armazenadas nele.

        Neste ponto do processo, o objetivo é serializar as configurações na interface IPropertyBag2 no arquivo RAW. Para fazer isso, é necessário girar um codificador e assim por diante, que é detalhado nas etapas a seguir.

    5.  Cria um [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) para o arquivo RAW.
    6.  Chama [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Inicializar**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize), passando um novo fluxo (em branco) para codificar.
    7.  Chama [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) para criar um novo IWICBitmapFrameEncode para o quadro RAW.
    8.  Chama [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Inicializa e**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)passa a interface IPropertyBag2 da etapa 4.
    9.  Chama [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) com [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) do quadro de imagem RAW do decodificador.
    10. Chama [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit). Em seguida, o codec serializa as propriedades no IPropertyBag2 da etapa 8 para o arquivo. Supõe-se que o método mais comum de serialização das propriedades seja escrevendo-as como metadados no arquivo.
    11. Chama [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).
    12. Chama IStream::Commit no fluxo na etapa 6.

    As configurações são serializadas no arquivo.

    Esse método incorre no custo de reescrever todo o arquivo RAW sempre que as configurações são serializadas. Isso pode ser evitado se você implementar [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) ou se o formato de arquivo de imagem for compatível com XMP ou EXIF, pois o WIC fornece [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) para ambos os formatos. Além disso, se o codec grava alterações no final do arquivo de imagem, você não acabará reescrevendo todo o arquivo de imagem.

-   Os conjuntos de parâmetros são carregados do estado serializado quando o aplicativo define a enumeração [**WICRawParameterSet.WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) no método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**LoadParameterSet.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) O [**sinalizador WICRawParameterSet.WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) refere-se ao último conjunto de parâmetros salvo, portanto, uma carga com esse sinalizador deve resultar na restauração de parâmetros para o estado salvo pela última vez.
-   Após a carga inicial, o conjunto de parâmetros salvo pela última vez deve ser carregado, se disponível. Caso não, as configurações "as-shot" deverão ser usadas como predefinições nas variáveis de interface [**IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Essas configurações de captura também podem ser carregadas usando o [**sinalizador WICRawParameterSet.WICAsShotParameterSet.**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset)
-   O identificador [**WICRawParameterSet.WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) deve representar uma configuração "Auto". O designer de codec pode escolher qualquer uma das seguintes abordagens sobre como definir parâmetros [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) quando essa configuração é feita:

    -   Execute uma otimização algorítmica de alguns parâmetros, como exposição ou cor. É assim que o Auto funciona em editores de imagem típicos e se baseia principalmente na análise de dados de pixel.
    -   Definir configurações de câmera semelhantes a como uma Configuração automática teria se comportado. Isso será útil se a imagem tiver sido gravado em uma configuração Manual e permitir que o usuário substitua as configurações manuais.
    -   Não fazer nada. Nem todos os controles precisam ser definidos quando Automático é selecionado e não há problema em deixar as configurações inalteradas.

As ferramentas de edição Windows Vista Galeria de Fotos e Windows Live Galeria de Fotos e outros aplicativos de edição usam a carga do parâmetro [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Auto quando o usuário seleciona Auto Correct para todos os ajustes de controle de codec normais, como cor e exposição, para obter os melhores resultados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem RAW da câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



