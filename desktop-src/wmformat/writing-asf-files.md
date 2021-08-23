---
title: Escrevendo arquivos ASF
description: Escrevendo arquivos ASF
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows SDK de Formato de Mídia, escrevendo arquivos ASF
- Windows SDK de Formato de Mídia, criando arquivos ASF
- Windows SDK de Formato de Mídia, FORMATO DE SISTEMAS Avançados (ASF)
- ASF (Advanced Systems Format), escrevendo arquivos
- ASF (Formato de Sistemas Avançados), escrevendo arquivos
- ASF (Advanced Systems Format), criando arquivos
- ASF (Formato de Sistemas Avançados), criando arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4bec466a9f38dfedaa7e860fdc5e3eda56e0ca5fa1f1240bc18c54dfd51513
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590616"
---
# <a name="writing-asf-files"></a>Escrevendo arquivos ASF

Você pode usar o objeto writer do SDK Windows Media Format para criar arquivos ASF de dados de mídia digital. Para criar uma instância do objeto writer, chame a [**função WMCreateWriter.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) O objeto writer coordena a funcionalidade de vários componentes, incluindo codecs, que são externos ao SDK Windows Formato de Mídia.

A funcionalidade básica do objeto writer pode ser dividida nas etapas a seguir. Nestas etapas, "o aplicativo" refere-se ao programa que você escreve usando o SDK Windows Formato de Mídia.

1.  O aplicativo fornece ao autor um perfil a ser usado na criação do arquivo ASF. Quando o autor carrega os dados do perfil, ele atribui um número de entrada a cada conexão do perfil.
2.  O aplicativo fornece ao autor um nome de arquivo de saída para o arquivo a ser gravado. O autor cria um objeto de sink de arquivo de autor para gerenciar a criação e a entrada do arquivo. Para obter mais informações, consulte [Writer File Sink Object](writer-file-sink-object.md).
3.  O autor cria um header para o novo arquivo com base nas informações no perfil.
4.  O aplicativo passa exemplos descompactados para o autor. Os exemplos são passados um de cada vez em buffers envolvidos em objetos de buffer. O aplicativo deve passar amostras para cada fluxo simultaneamente para que o autor receba todos os exemplos em ordem de tempo de apresentação.
5.  O autor passa os exemplos para o codec apropriado para compactação. Quando o autor recebe os exemplos compactados, ele os intercala com exemplos de outros fluxos para que os exemplos acessem o arquivo em ordem de tempo de apresentação, independentemente do fluxo. Os dados de exemplo são então feitos em pacotes e gravados na seção de dados do arquivo.
6.  Quando todos os exemplos são processados, o autor pode adicionar um índice ao arquivo para melhorar o desempenho de busca.

Essas etapas são ilustradas no aplicativo de exemplo WMStats, entre outros. Para obter mais informações, consulte [Aplicativos de exemplo](sample-applications.md).

O autor também dá suporte à funcionalidade mais avançada, permitindo que você faça o seguinte:

-   Edite metadados no header do arquivo.
-   Escreva exemplos pré-compactados.
-   Gravar em sinks de rede para transmitir dados ao vivo.
-   Gravar em sinks de arquivos para opções avançadas de controle de arquivos.
-   Gravar em sinks push para distribuição para servidores que fornecerão conteúdo aos usuários finais.
-   Entregar exemplos de postview para verificação da saída.
-   Fornecer estatísticas de desempenho do autor.

As seções a seguir descrevem o uso do objeto writer em detalhes.



| Seção                                                                    | Descrição                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Usar perfis com o gravador](to-use-profiles-with-the-writer.md)     | Descreve como especificar um perfil a ser usado com o autor.                                             |
| [Trabalhando com entradas](working-with-inputs.md)                             | Descreve como identificar e definir as configurações de entrada no autor.                              |
| [Para editar metadados com o writer](to-edit-metadata-with-the-writer.md)   | Descreve como usar o writer para editar metadados para um novo arquivo.                                       |
| [Para gravar exemplos](to-write-samples.md)                                   | Descreve como passar amostras para o autor.                                                           |
| [Configurando extensões de unidade de dados](setting-data-unit-extensions.md)           | Descreve como adicionar dados estendidos a exemplos.                                                         |
| [Escrevendo exemplos compactados](writing-compressed-samples.md)               | Descreve como passar amostras pré-compactadas para o autor.                                            |
| [Escrevendo imagens Fluxos](writing-image-streams.md)                         | Descreve como configurar uma entrada para um fluxo de imagem.                                               |
| [Escrevendo exemplos de imagem de vídeo](writing-video-image-samples.md)             | Descreve como configurar exemplos de Imagem de Vídeo.                                                        |
| [Escrevendo a taxa de bits variável Fluxos](writing-variable-bit-rate-streams.md) | Descreve como gravar fluxos de VBR (taxa de bits variável).                                                |
| [Usando Two-Pass codificação](using-two-pass-encoding.md)                     | Descreve como fazer com que o codec execute uma aprovação preliminar antes de escrever o arquivo.                    |
| [Para forçar Key-Frame inserção](to-force-key-frame-insertion.md)           | Descreve como forçar manualmente o codec a codificar um exemplo como um quadro-chave.                           |
| [Para gerenciar a latência do writer](to-manage-writer-latency.md)                   | Descreve como minimizar o tempo necessário para o autor processar amostras em um arquivo de saída ou um sink. |
| [Trabalhando com os sinks do Writer](working-with-writer-sinks.md)                 | Descreve como usar os sinks de writer para entregar seu conteúdo a arquivos ou locais de rede.               |
| [Para obter estatísticas do writer](to-get-writer-statistics.md)                   | Descreve como obter estatísticas para o autor.                                                        |
| [Para usar o Postview do Writer](to-use-writer-postview.md)                       | Descreve como obter exemplos descompactados à medida que você escreve um arquivo para verificação.                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> <dt>

[**Objeto de coletor de arquivo do gravador**](writer-file-sink-object.md)
</dt> <dt>

[**Objeto do Sink de Rede do Writer**](writer-network-sink-object.md)
</dt> <dt>

[**Objeto do gravador**](writer-object.md)
</dt> </dl>

 

 




