---
title: Uso de coletores de arquivos
description: Uso de coletores de arquivos
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- FORMATO DE SISTEMAS Avançados (ASF), sinks de arquivos
- ASF (Formato de Sistemas Avançados), sinks de arquivos
- ASF (Advanced Systems Format), sinks
- ASF (Formato de Sistemas Avançados), sinks
- sinks,file sinks
- sinks de arquivo, sobre
- sinks de arquivo, criando
- sinks de arquivo, parando
- sinks de arquivo, iniciando
- sinks de arquivo, fechamento
- sinks,statistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f94bd6698ca30a645957da36cf3b81a84f9d3e7c8ce6c598be2c39f8ac766db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196169"
---
# <a name="using-file-sinks"></a>Uso de coletores de arquivos

Em circunstâncias normais, você pode simplesmente passar ao autor um nome de arquivo de saída usando o método [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) e o objeto writer gravará o arquivo no disco automaticamente. Nesse caso, o autor está, na verdade, criando e controlando um objeto de sink de arquivo de autor que lida com a escrita do arquivo no disco. Um objeto de sink de arquivo de autor controla o fluxo de dados do objeto writer para um único arquivo.

Você pode criar seus próprios sinks de arquivo para obter mais controle sobre como o sink grava o arquivo. Você também pode acessar o sink de arquivo de autor padrão criado pelo autor em resposta a uma chamada para **SetOutputFilename**.

## <a name="creating-file-sinks"></a>Criando os sinks de arquivos

Para criar um sink de arquivo e adicioná-lo ao autor, execute as etapas a seguir.

1.  Crie um novo sink chamando a [**função WMCreateWriterFileSink.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)
2.  Fornecer um nome de arquivo para o sink chamando [**IWMWriterFileSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).
3.  Adicione o sink de arquivo ao autor chamando [**IWMWriterAdvanced::AddSink.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink)
4.  Execute a escrita da maneira normal.
5.  Após a conclusão da escrita, o sink fechará o arquivo automaticamente.

## <a name="stopping-and-starting-file-sinks"></a>Parando e iniciando os sinks de arquivos

Após o início das operações de escrita, você pode parar de escrever em um sink de arquivos chamando [**IWMWriterFileSink2::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).

Há muitos motivos potenciais pelos quais você deseja parar de escrever em um sink. Por exemplo, se você estiver gravando de uma fonte ao vivo, poderá estar interessado apenas em parte do conteúdo.

Você pode retomar a escrita em um sink de arquivo chamando [**IWMWriterFileSink2::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start). Os **tempos de** apresentação Parar e Iniciar usam para controlar aproximadamente quando o comando é executado.  Você pode usar os [**métodos IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) para obter mais controle sobre os horários de início e de parada.

## <a name="closing-file-sinks"></a>Fechando os sinks de arquivo

Normalmente, um sink de arquivo é fechado automaticamente. Se você terminar de escrever em um sink, mas as operações de escrita em outros sinks continuarem, deverá fechar explicitamente o sink para conservar recursos. Para fechar um sink de arquivo, chame [**IWMWriterFileSink2::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).

## <a name="getting-sink-statistics"></a>Obter estatísticas do sink

Você pode obter o tamanho e a duração do arquivo para um sink aberto chamando [**IWMWriterFileSink2::GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) e [**IWMWriterFileSink2::GetFileDuration,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectivamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMWriterFileSink Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[**IWMWriterFileSink2 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[**IWMWriterFileSink3 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[**Objeto de coletor de arquivo do gravador**](writer-file-sink-object.md)
</dt> <dt>

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




