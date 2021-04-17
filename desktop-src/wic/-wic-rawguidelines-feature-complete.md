---
description: 'Integridade do recurso: interfaces recomendadas'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Integridade do recurso: interfaces recomendadas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1dba4bcc029b2205985afb443526376c0eecb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813311"
---
# <a name="feature-completeness-recommended-interfaces"></a>Integridade do recurso: interfaces recomendadas

A tabela a seguir lista os codecs BRUTOs de interfaces do Windows Imaging Component (WIC) que devem ser implementados.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Interface</th>
<th>Obrigatório para</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></td>
<td>Decodificadores</td>
<td>Representa o ponto de partida para a decodificação de um arquivo de imagem. Fornece acesso a propriedades de nível de contêiner como miniaturas, quadros e paleta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></td>
<td>Decodificadores</td>
<td>Representa um quadro de imagem específico dentro do contêiner que fornece acesso a propriedades em nível de quadro. Essa é a interface que decodifica os bits de imagem reais.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></td>
<td>Decodificadores</td>
<td>Necessário para enumerar e iterar por meio de blocos de metadados e invocar os leitores de metadados apropriados ao ler de um arquivo de imagem. <br/>
<blockquote>
[!Note]<br />
Se o formato de contêiner bruto for compatível com TIFF ou usar IFDs ou IRBs padrão para armazenar metadados EXIF ou XMP, os autores de codec poderão optar por invocar os leitores de metadados internos em vez de escrever seus próprios.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></td>
<td>Decodificadores</td>
<td>Permite que o chamador especifique o formato de escala, corte, rotação ou pixel desejado para a imagem decodificada, o que pode melhorar significativamente o desempenho do decodificador. Por exemplo, os decodificadores de JPEG e WDP (protocolo de datagrama sem fio) da Microsoft usam um esquema de otimização de pirâmide para obter uma decodificação mais rápida quando o bitmap de destino é menor do que o bitmap de origem. O Windows Vista (e posterior) tentará usar essa interface para extrair uma &quot; &quot; visualização rápida de uma imagem bruta sempre que a visualização inserida estiver faltando ou tiver menos de 1.024 pixels em sua dimensão maior.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></td>
<td>Decodificadores</td>
<td>Necessário para formatos BRUTOs. Expõe parâmetros que são específicos do processamento de imagem bruto. Os codecs BRUTOs devem dar suporte a quantos desses parâmetros forem aplicados ao codec.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></td>
<td>Codificadores</td>
<td>Representa o ponto de partida para codificar um arquivo de imagem. Essa interface é usada para definir propriedades em nível de contêiner, como miniaturas, quadros e paleta. Também é necessário invocar um gravador de metadados para habilitar a persistência de metadados para o arquivo de imagem. Por esses motivos, essa interface é necessária mesmo que a codificação do bitmap primário para o formato bruto não seja suportada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></td>
<td>Codificadores</td>
<td>Representa um quadro de imagem específico dentro do contêiner. Essa interface é usada para codificar os bits de imagem reais e para definir as propriedades e os metadados por quadro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></td>
<td>Codificadores</td>
<td>Necessário para iterar por meio de blocos de metadados e invocar os gravadores de metadados apropriados ao serializar um arquivo de imagem.<br/>
<blockquote>
[!Note]<br />
Se o formato de contêiner bruto for compatível com TIFF, os autores de codec poderão optar por invocar os gravadores de metadados internos em vez de escrever seus próprios.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

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

 

 




