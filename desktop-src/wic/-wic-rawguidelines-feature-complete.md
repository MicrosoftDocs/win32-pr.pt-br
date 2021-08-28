---
description: 'Integridade do recurso: interfaces recomendadas'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Integridade do recurso: interfaces recomendadas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c819f56b9343eab8326eb755d86280bde242a01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473822"
---
# <a name="feature-completeness-recommended-interfaces"></a>Integridade do recurso: interfaces recomendadas

a tabela a seguir lista os codecs brutos das interfaces do componente de Windows Imaging (WIC) que devem ser implementados.




| Interface | Obrigatório para | Descrição | 
|-----------|--------------|-------------|
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a> | Decodificadores | Representa o ponto de partida para a decodificação de um arquivo de imagem. Fornece acesso a propriedades de nível de contêiner como miniaturas, quadros e paleta.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a> | Decodificadores | Representa um quadro de imagem específico dentro do contêiner que fornece acesso a propriedades em nível de quadro. Essa é a interface que decodifica os bits de imagem reais.<br /> | 
| <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> | Decodificadores | Necessário para enumerar e iterar por meio de blocos de metadados e invocar os leitores de metadados apropriados ao ler de um arquivo de imagem. <br /><blockquote>[!Note]<br />Se o formato de contêiner bruto for compatível com TIFF ou usar IFDs ou IRBs padrão para armazenar metadados EXIF ou XMP, os autores de codec poderão optar por invocar os leitores de metadados internos em vez de escrever seus próprios.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a> | Decodificadores | Permite que o chamador especifique o formato de escala, corte, rotação ou pixel desejado para a imagem decodificada, o que pode melhorar significativamente o desempenho do decodificador. Por exemplo, os decodificadores de JPEG e WDP (protocolo de datagrama sem fio) da Microsoft usam um esquema de otimização de pirâmide para obter uma decodificação mais rápida quando o bitmap de destino é menor do que o bitmap de origem. Windows O Vista (e posterior) tentará usar essa interface para extrair uma visualização "rápida" de uma imagem bruta sempre que a visualização inserida estiver faltando ou tiver menos de 1.024 pixels em sua dimensão maior.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a> | Decodificadores | Necessário para formatos BRUTOs. Expõe parâmetros que são específicos do processamento de imagem bruto. Os codecs BRUTOs devem dar suporte a quantos desses parâmetros forem aplicados ao codec.<br /> | 
| <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a> | Codificadores | Representa o ponto de partida para codificar um arquivo de imagem. Essa interface é usada para definir propriedades em nível de contêiner, como miniaturas, quadros e paleta. Também é necessário invocar um gravador de metadados para habilitar a persistência de metadados para o arquivo de imagem. Por esses motivos, essa interface é necessária mesmo que a codificação do bitmap primário para o formato bruto não seja suportada.<br /> | 
| <a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a> | Codificadores | Representa um quadro de imagem específico dentro do contêiner. Essa interface é usada para codificar os bits de imagem reais e para definir as propriedades e os metadados por quadro.<br /> | 
| <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> | Codificadores | Necessário para iterar por meio de blocos de metadados e invocar os gravadores de metadados apropriados ao serializar um arquivo de imagem.<br /><blockquote>[!Note]<br />Se o formato de contêiner bruto for compatível com TIFF, os autores de codec poderão optar por invocar os gravadores de metadados internos em vez de escrever seus próprios.</blockquote><br /><br /> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Windows Visão geral do componente de geração de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem bruta de câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




