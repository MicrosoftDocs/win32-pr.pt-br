---
title: Para criar um leitor e abrir um arquivo
description: Para criar um leitor e abrir um arquivo
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- ASF (Advanced Systems Format), criando leitores
- ASF (formato de sistemas avançados), criando leitores
- Formato de sistema avançado (ASF), abertura de arquivos
- ASF (formato de sistemas avançados), abrindo arquivos
- leitores assíncronos, criando
- leitores assíncronos, abrindo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640296"
---
# <a name="to-create-a-reader-and-open-a-file"></a>Para criar um leitor e abrir um arquivo

Antes de poder fazer qualquer trabalho com o leitor, você precisará criar um objeto leitor e carregar um arquivo para leitura. Para inicializar o leitor e abrir um arquivo, execute as etapas a seguir.

1.  Crie um objeto leitor chamando a função [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) . Você deve especificar o nível desejado de gerenciamento de direitos para o novo objeto de leitor. Os modos disponíveis são listados no tipo de enumeração [**\_ direitos WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .
2.  Especifique um arquivo para ler chamando [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open). Você deve especificar uma interface de retorno de chamada de leitura para o leitor usar. Para obter mais informações sobre o retorno de chamada de leitor, consulte [para implementar mensagens de leitor no retorno de chamada OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md).
3.  Aguarde até que o leitor Abra o arquivo. Quando você chama **Open** para carregar um arquivo, ele retorna quase imediatamente e continua o processamento em outro thread. Você deve aguardar a conclusão das operações, sinalizando um evento quando o retorno de chamada **OnStatus** receber a \_ mensagem de status WMT aberta.

O leitor também dá suporte ao uso da interface com de **IStream** para abrir arquivos. Você pode implementar a interface **IStream** da maneira que escolher. Depois que o arquivo desejado for aberto em **IStream**, você poderá seguir as etapas listadas acima, exceto pelo fato de que você deve chamar [**IWMReaderAdvanced2:: OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) em vez de **IWMReader:: Open** na etapa 2.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interface IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Interface IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[**Lendo arquivos com o leitor assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Usando os métodos de retorno de chamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




