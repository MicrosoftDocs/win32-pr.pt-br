---
title: Gravando arquivos ASF
description: Gravando arquivos ASF
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows Media Format SDK, gravando arquivos ASF
- SDK do Windows Media Format, criando arquivos ASF
- SDK do Windows Media Format, formato de sistemas avançados (ASF)
- ASF (Advanced Systems Format), gravando arquivos
- ASF (formato de sistemas avançados), gravando arquivos
- ASF (Advanced Systems Format), criando arquivos
- ASF (formato de sistemas avançados), criando arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c13c1af0d3699c89d26f007e00675ea563639c4e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823564"
---
# <a name="writing-asf-files"></a>Gravando arquivos ASF

Você pode usar o objeto gravador do SDK do Windows Media Format para criar arquivos ASF a partir de dados de mídia digital. Para criar uma instância do objeto Writer, chame a função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . O objeto Writer coordena a funcionalidade de vários componentes, incluindo codecs, que são externos ao Windows Media Format SDK.

A funcionalidade básica do objeto gravador pode ser dividida nas etapas a seguir. Nestas etapas, "o aplicativo" refere-se ao programa que você escreve usando o SDK do Windows Media Format.

1.  O aplicativo fornece ao gravador um perfil a ser usado na criação do arquivo ASF. Quando o gravador carrega os dados de perfil, ele atribui um número de entrada a cada conexão do perfil.
2.  O aplicativo fornece ao gravador um nome de arquivo de saída para o arquivo a ser gravado. O gravador cria um objeto de coletor de arquivo do gravador para gerenciar a criação e a entrada do arquivo. Para obter mais informações, consulte [objeto de coletor de arquivo do gravador](writer-file-sink-object.md).
3.  O gravador cria um cabeçalho para o novo arquivo com base nas informações do perfil.
4.  O aplicativo passa amostras descompactadas para o gravador. Os exemplos são passados um de cada vez em buffers encapsulados em objetos de buffer. O aplicativo deve passar amostras para cada fluxo simultaneamente para que o gravador receba todos os exemplos em ordem de tempo de apresentação.
5.  O gravador passa os exemplos para o codec apropriado para compactação. Quando o gravador recebe os exemplos compactados, ele os intercala com exemplos de outros fluxos, de modo que os exemplos vão para o arquivo na ordem de tempo da apresentação, independentemente do fluxo. Os dados de exemplo são então feitos em pacotes e gravados na seção de dados do arquivo.
6.  Quando todas as amostras são processadas, o gravador pode adicionar um índice ao arquivo para melhorar o desempenho de busca.

Essas etapas são ilustradas no aplicativo de exemplo WMStats, entre outras. Para obter mais informações, consulte [aplicativos de exemplo](sample-applications.md).

O gravador também dá suporte à funcionalidade mais avançada, permitindo que você faça o seguinte:

-   Edite metadados no cabeçalho do arquivo.
-   Escreva amostras precompactadas.
-   Gravar em coletores de rede para streaming de dados dinâmicos.
-   Gravar em coletores de arquivo para opções avançadas de controle de arquivo.
-   Gravar em coletores de push para distribuição para servidores que fornecerão conteúdo aos usuários finais.
-   Forneça exemplos de exibição prévia para verificação da saída.
-   Entregar as estatísticas de desempenho do gravador.

As seções a seguir descrevem o uso do objeto do gravador em detalhes.



| Seção                                                                    | Descrição                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Usar perfis com o gravador](to-use-profiles-with-the-writer.md)     | Descreve como especificar um perfil a ser usado com o gravador.                                             |
| [Trabalhando com entradas](working-with-inputs.md)                             | Descreve como identificar e definir as configurações de entrada no gravador.                              |
| [Para editar metadados com o gravador](to-edit-metadata-with-the-writer.md)   | Descreve como usar o gravador para editar metadados para um novo arquivo.                                       |
| [Para escrever exemplos](to-write-samples.md)                                   | Descreve como passar amostras para o gravador.                                                           |
| [Definindo extensões de unidade de dados](setting-data-unit-extensions.md)           | Descreve como adicionar dados estendidos a exemplos.                                                         |
| [Gravando amostras compactadas](writing-compressed-samples.md)               | Descreve como passar amostras compactadas previamente para o gravador.                                            |
| [Gravando fluxos de imagem](writing-image-streams.md)                         | Descreve como configurar uma entrada para um fluxo de imagem.                                               |
| [Escrevendo amostras de imagens de vídeo](writing-video-image-samples.md)             | Descreve como configurar exemplos de imagem de vídeo.                                                        |
| [Gravando fluxos de taxa de bits variáveis](writing-variable-bit-rate-streams.md) | Descreve como gravar fluxos de taxa de bits variável (VBR).                                                |
| [Usando a codificação Two-Pass](using-two-pass-encoding.md)                     | Descreve como fazer com que o codec execute uma passagem preliminar antes de gravar o arquivo.                    |
| [Para forçar a inserção de Key-Frame](to-force-key-frame-insertion.md)           | Descreve como forçar manualmente o codec para codificar um exemplo como um quadro-chave.                           |
| [Para gerenciar a latência do gravador](to-manage-writer-latency.md)                   | Descreve como minimizar o tempo que o gravador leva para processar amostras em um arquivo ou coletor de saída. |
| [Trabalhando com coletores de gravador](working-with-writer-sinks.md)                 | Descreve como usar coletores de gravador para entregar seu conteúdo a arquivos ou locais de rede.               |
| [Para obter estatísticas do gravador](to-get-writer-statistics.md)                   | Descreve como obter estatísticas para o gravador.                                                        |
| [Para usar a exibição do gravador](to-use-writer-postview.md)                       | Descreve como obter amostras não compactadas à medida que você escreve um arquivo para verificação.                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> <dt>

[**Objeto de coletor de arquivo do gravador**](writer-file-sink-object.md)
</dt> <dt>

[**Objeto de coletor de rede do gravador**](writer-network-sink-object.md)
</dt> <dt>

[**Objeto do gravador**](writer-object.md)
</dt> </dl>

 

 




