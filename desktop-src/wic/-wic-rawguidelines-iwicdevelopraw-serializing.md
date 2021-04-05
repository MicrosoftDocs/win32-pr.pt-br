---
description: Diretrizes de implementação para a serialização de configurações de IWICDevelopRaw
ms.assetid: 4ecff5cc-24f3-4b89-b681-85c867b053e7
title: Diretrizes de implementação para a serialização de configurações de IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48cdc78f68e6d63ee7870b9296ae4cfa4f85547a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662753"
---
# <a name="implementation-guidelines-for-serializing-iwicdevelopraw-settings"></a>Diretrizes de implementação para a serialização de configurações de IWICDevelopRaw

A interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expõe as configurações que o aplicativo pode usar para modificar o processamento da imagem bruta. As configurações devem poder ser serializadas para que persistam entre as sessões. Embora isso possa ser feito de várias maneiras, é recomendável codificar esses dados de uma maneira que seja consistente com outros metadados.

A seguir estão algumas diretrizes gerais de implementação:

-   As configurações feitas por meio de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) (como rotação ou balanço de branco) devem evitar a substituição da configuração da câmera ou dos dados "como capturados", a menos que a marca seja normalmente usada como "configuração atual". Por exemplo, as marcas de orientação de EXIF podem ser usadas para persistir a rotação.
-   É preferível não precisar salvar todo o arquivo (incluindo os dados de pixel do mosaico) toda vez que as configurações de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) são solicitadas para serem serializadas.
-   O processo de serialização de configurações de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) geralmente seguirá essa ordem de eventos. O aplicativo:

    1.  Cria uma instância de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) em um arquivo bruto.
    2.  Chama [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) para obter um [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) para o quadro bruto.
    3.  Chama QueryInterface na interface IWICBitmapFrameDecode para a interface IWICDevelopRaw.
    4.  Chama [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), que retorna uma interface IPropertyBag2 com todas as propriedades atuais armazenadas nela.

        Nesse ponto do processo, o objetivo é serializar as configurações na interface IPropertyBag2 para o arquivo bruto. Para isso, é necessário girar um codificador e assim por diante, que é detalhado nas etapas a seguir.

    5.  Cria um [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) para o arquivo bruto.
    6.  Chama [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize), passando um novo fluxo (em branco) para codificar.
    7.  Chama [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) para criar um novo IWICBITMAPFRAMEENCODE para o quadro bruto.
    8.  Chama [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)e passa na interface IPropertyBag2 da etapa 4.
    9.  Chama [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**WriteName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) com [**IWICBITMAPSOURCE**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) do quadro da imagem bruta do decodificador.
    10. Chama [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit). Em seguida, o codec serializa as propriedades no IPropertyBag2 da etapa 8 para o arquivo. Presume-se que o método mais comum de serialização das propriedades esteja gravando-as como metadados no arquivo.
    11. Chama [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).
    12. Chama IStream:: Commit no fluxo na etapa 6.

    As configurações são serializadas no arquivo.

    Esse método incorre no custo de regravação de todo o arquivo bruto sempre que as configurações são serializadas. Isso pode ser evitado se você implementar [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) ou se o formato de arquivo de imagem der suporte a XMP ou EXIF, pois o WIC fornece [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) para ambos os formatos. Além disso, se o codec gravar alterações no final do arquivo de imagem, você não acabará regravando todo o arquivo de imagem.

-   Os conjuntos de parâmetros são carregados a partir do estado serializado quando o aplicativo define a enumeração [**WICRawParameterSet. WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) no método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**parameterset**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) . O sinalizador [**WICRawParameterSet. WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) refere-se ao último conjunto de parâmetros salvo, portanto, uma carga com esse sinalizador deve resultar na restauração de parâmetros para o último estado salvo.
-   Após o carregamento inicial, o último conjunto de parâmetros salvo deve ser carregado, se disponível. Caso contrário, as configurações "as-shot" devem ser usadas como predefinições nas variáveis de interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . Essas configurações como capturadas também podem ser carregadas usando o sinalizador [**WICRawParameterSet. WICAsShotParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) .
-   O identificador [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) destina-se a representar uma configuração "automática". O designer de codec pode eleger qualquer uma das seguintes abordagens sobre como definir parâmetros [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) quando essa configuração é feita:

    -   Execute uma otimização de algoritmos de alguns parâmetros, como exposição ou cor. É assim que as funções automáticas nos editores de imagem típicos e baseiam-se principalmente na análise de dados de pixel.
    -   Defina configurações de câmera semelhantes a como uma configuração automática teria se compareceda. Isso é útil se a imagem foi capturada em uma configuração manual e permite que o usuário substitua as configurações manuais.
    -   Não fazer nada. Nem todos os controles precisam ser definidos quando auto é selecionado e OK para deixar as configurações inalteradas.

A Galeria de fotos do Windows Vista e as ferramentas de edição da Galeria de fotos do Windows Live e outros aplicativos de edição usam o carregamento de parâmetro automático [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) quando o usuário seleciona a correção automática para todos os ajustes de controle de codec normais, como cor e exposição, para obter os melhores resultados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem bruta de câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



