---
description: Divisor de ASF
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: Divisor de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089798"
---
# <a name="asf-splitter"></a>Divisor de ASF

O objeto *divisor* de ASF é um componente de camada WMContainer que analisa o objeto de dados ASF de um arquivo ASF (Advanced Systems Format). Você pode usar o divisor para ler os pacotes de dados no objeto de dados e gerar amostras de fluxo. Para obter informações sobre a estrutura de um arquivo ASF, consulte [estrutura de arquivo ASF](asf-file-structure.md).

O divisor expõe a interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) . O divisor analisa os pacotes de dados ASF para os fluxos selecionados e os reempacota em objetos de exemplo individuais que expõem a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) . O divisor é um dos componentes de nível de plataforma do Media Foundation. A fonte de mídia do ASF usa o divisor internamente para analisar arquivos ASF.

O diagrama a seguir ilustra a geração de amostra para um arquivo ASF por meio do divisor.

![diagrama mostrando a geração de exemplo de um arquivo ASF](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

Esta seção contém os seguintes tópicos:



| Tópico                                                                                                                        | Descrição                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Criando o objeto divisor de ASF](creating-the-asf-splitter-object.md)                                                     | Como criar e inicializar o divisor.                              |
| [Configurando o objeto divisor de ASF](configuring-the-asf-splitter-object.md)                                               | Definições de configuração para o divisor.                                |
| [Gerando amostras de fluxo de um objeto de dados ASF existente](generating-stream-samples-from-an-existing-asf-data-object.md) | Como analisar o objeto de dados ASF e gerar amostras de fluxo em pacotes. |



 

A tabela a seguir mostra os atributos de objeto de dados relevantes.



| Atributo                                                                                                    | Descrição                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ pacotes FileProperties do MF PD ASF \_**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Número de pacotes de dados no objeto de dados ASF.                                                       |
| [**\_tamanho de \_ \_ pacote FileProperties \_ min \_ do MF PD ASF \_**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Tamanho mínimo dos pacotes de dados no arquivo, em bytes.                                              |
| [**\_ \_ \_ \_ tamanho máximo do pacote FileProperties \_ do MF PD ASF \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Tamanho máximo dos pacotes de dados no arquivo, em bytes                                               |
| [**\_comprimento de \_ \_ dados ASF \_ do MF PD**](mf-pd-asf-data-length-attribute.md)                                         | Tamanho do objeto de dados ASF, em bytes.                                                               |
| [**deslocamento de início de dados do MF \_ PD \_ ASF \_ \_ \_**](mf-pd-asf-data-start-offset-attribute.md)                            | Deslocamento, em bytes, para o primeiro pacote de dados no objeto de dados ASF relativo ao início do arquivo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes ASF WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Tutorial: lendo um arquivo ASF](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



