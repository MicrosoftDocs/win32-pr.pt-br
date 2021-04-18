---
title: Para criar um leitor síncrono e abrir um arquivo
description: Para criar um leitor síncrono e abrir um arquivo
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- ASF (Advanced Systems Format), criando leitores
- ASF (formato de sistemas avançados), criando leitores
- Formato de sistema avançado (ASF), abertura de arquivos
- ASF (formato de sistemas avançados), abrindo arquivos
- leitores síncronos, criando
- leitores síncronos, abrindo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105797902"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a>Para criar um leitor síncrono e abrir um arquivo

Antes de poder fazer qualquer trabalho com o leitor síncrono, você precisará criar um objeto leitor síncrono e carregar um arquivo para leitura. Para inicializar o leitor síncrono e abrir um arquivo, execute as etapas a seguir.

1.  Crie um objeto leitor síncrono chamando a função [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) . Você deve especificar o nível desejado de gerenciamento de direitos para o novo objeto de leitor. Os modos disponíveis são listados no tipo de enumeração **\_ direitos WMT** .
2.  Especifique um arquivo para ler chamando [**IWMSyncReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).

O leitor síncrono também dá suporte ao uso da interface com de **IStream** para abrir arquivos. Você pode implementar a interface **IStream** da maneira que escolher. Depois que o arquivo desejado for aberto em **IStream**, você poderá seguir as etapas listadas acima, exceto pelo fato de que você deve chamar [**IWMSyncReader:: OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) em vez de **IWMSyncReader:: Open** na etapa 2.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lendo arquivos com o leitor síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




