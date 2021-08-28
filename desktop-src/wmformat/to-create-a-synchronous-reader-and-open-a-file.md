---
title: Para criar um leitor síncrono e abrir um arquivo
description: Para criar um leitor síncrono e abrir um arquivo
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- ASF (Advanced Systems Format), criando leitores
- ASF (Formato de Sistemas Avançados), criando leitores
- ASF (Advanced Systems Format), abrindo arquivos
- ASF (Formato de Sistemas Avançados), abrindo arquivos
- leitores síncronos, criando
- leitores síncronos, abrindo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d1c6897c05bb0d843e5818f078df5235a5afac4a485d6a719ab86b8e4f8267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807646"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a>Para criar um leitor síncrono e abrir um arquivo

Antes de poder trabalhar com o leitor síncrono, você precisará criar um objeto de leitor síncrono e carregar um arquivo para leitura. Para inicializar o leitor síncrono e abrir um arquivo, execute as etapas a seguir.

1.  Crie um objeto de leitor síncrono chamando a [**função WMCreateSyncReader.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) Você deve especificar o nível desejado de gerenciamento de direitos para o novo objeto de leitor. Os modos disponíveis são listados no tipo de **enumeração WMT \_ RIGHTS.**
2.  Especifique um arquivo a ser lido chamando [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).

O leitor síncrono também dá suporte ao uso da interface COM **IStream** para abrir arquivos. Você pode implementar a interface **IStream** da maneira que você escolher. Depois que o arquivo desejado for aberto no **IStream,** você poderá seguir as etapas listadas acima, exceto que você deve chamar [**IWMSyncReader::OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) em vez de **IWMSyncReader::Open** na etapa 2.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMSyncReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lendo arquivos com o Leitor Síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




