---
title: Uso de coletores de arquivos
description: Uso de coletores de arquivos
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- ASF (Advanced Systems Format), coletores de arquivos
- ASF (formato de sistemas avançados), coletores de arquivo
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- coletores, coletores de arquivos
- coletores de arquivos, sobre
- coletores de arquivos, criando
- coletores de arquivos, parando
- coletores de arquivos, iniciando
- coletores de arquivos, fechando
- coletores, estatísticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104084395"
---
# <a name="using-file-sinks"></a>Uso de coletores de arquivos

Em circunstâncias normais, você pode simplesmente passar o gravador um nome de arquivo de saída usando o método [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) e o objeto gravador gravará o arquivo em disco automaticamente. Nesse caso, o gravador está, na verdade, criando e controlando um objeto de coletor de arquivo do gravador que manipula a gravação do arquivo em disco. Um objeto de coletor de arquivo do gravador controla o fluxo de dados do objeto gravador para um único arquivo.

Você pode criar seus próprios coletores de arquivos para obter mais controle sobre como o coletor grava o arquivo. Você também pode acessar o coletor de arquivo de gravador padrão criado pelo gravador em resposta a uma chamada para **SetOutputFilename**.

## <a name="creating-file-sinks"></a>Criando coletores de arquivo

Para criar um coletor de arquivos e adicioná-lo ao gravador, execute as etapas a seguir.

1.  Crie um novo coletor chamando a função [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) .
2.  Forneça um nome de arquivo para o coletor chamando [**IWMWriterFileSink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).
3.  Adicione o coletor de arquivo ao gravador chamando [**IWMWriterAdvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).
4.  Execute escrita da maneira usual.
5.  Depois que a gravação for concluída, o coletor fechará o arquivo automaticamente.

## <a name="stopping-and-starting-file-sinks"></a>Parando e iniciando coletores de arquivo

Depois que as operações de gravação começam, você pode parar de gravar em um coletor de arquivos chamando [**IWMWriterFileSink2:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).

Há muitas razões possíveis pelas quais você desejaria parar de gravar em um coletor. Por exemplo, se você estiver gravando de uma fonte dinâmica, você só poderá estar interessado em parte do conteúdo.

Você pode retomar a gravação em um coletor de arquivos chamando [**IWMWriterFileSink2:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start). Ambos **param** e **começam** a usar os tempos de apresentação para controlar aproximadamente quando o comando é executado. Você pode usar os métodos [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) para obter mais controle sobre os horários de início e de parada.

## <a name="closing-file-sinks"></a>Fechando coletores de arquivo

Normalmente, um coletor de arquivos é fechado automaticamente. Se você terminar de gravar em um coletor, mas a gravação de operações em outros coletores estiver continuando, você deverá fechar explicitamente o coletor para conservar os recursos. Para fechar um coletor de arquivos, chame [**IWMWriterFileSink2:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).

## <a name="getting-sink-statistics"></a>Obtendo estatísticas do coletor

Você pode obter o tamanho do arquivo e a duração de um coletor aberto chamando [**IWMWriterFileSink2:: GetFiles**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) e [**IWMWriterFileSink2:: GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectivamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[**Interface IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[**Interface IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[**Objeto de coletor de arquivo do gravador**](writer-file-sink-object.md)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




