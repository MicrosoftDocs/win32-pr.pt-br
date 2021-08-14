---
title: Suporte de exemplo alocado pelo usuário
description: Suporte de exemplo alocado pelo usuário
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Windows SDK de Formato de Mídia, suporte de exemplo alocado pelo usuário
- ASF (Advanced Systems Format), suporte de exemplo alocado pelo usuário
- ASF (Formato de Sistemas Avançados), suporte de exemplo alocado pelo usuário
- suporte de exemplo alocado pelo usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8cba2d20586cc47845d961e5c92a0138a37d5d0db07feb23dbb68dda1b72eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845250"
---
# <a name="user-allocated-sample-support"></a>Suporte de exemplo alocado pelo usuário

Em circunstâncias normais, o objeto leitor e o objeto de leitor síncrono criam um novo objeto de buffer para cada amostra entregue ao seu aplicativo. Isso acontece porque o objeto de leitura não tem como saber o que seu aplicativo faz com os exemplos depois de obtém-los. Embora muitos aplicativos leiam exemplos apenas para renderizar imediatamente, alguns aplicativos talvez precisem manter amostras por um longo tempo. O objeto de leitura não pode, portanto, reutilizar nenhum dos buffers alocados; ele os entrega ao seu aplicativo, que, em seguida, tem controle sobre eles.

O problema com essa abordagem é que um arquivo pode conter um grande número de amostras. Se cada um deles exigir que um novo objeto de buffer seja criado, muito tempo do processador será perdido alocando e liberando memória. Em aplicativos sensíveis ao tempo, como players de mídia, essa sobrecarga pode ser muito prejudicial ao desempenho.

Para atenuar os problemas de desempenho de exemplos alocados pelo leitor, o leitor e o leitor síncrono são suportados por exemplos alocados pelo usuário. Para usar exemplos alocados pelo seu aplicativo, o objeto de leitura faz chamadas para um método de retorno de chamada de alocação de exemplo que você implementa. A lógica usada pelo retorno de chamada para entregar buffers para o objeto de leitura depende totalmente de você. Você pode usar um pool de buffers para todo o arquivo ou usar vários pools de buffers, um para cada saída ou fluxo ou qualquer outro esquema que funcione para seu aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Alocando buffers para leitura de arquivo**](allocating-buffers-for-file-reading.md)
</dt> <dt>

[**Recursos de leitura de arquivo**](file-reading-features.md)
</dt> </dl>

 

 




