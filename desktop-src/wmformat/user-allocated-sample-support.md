---
title: Suporte de amostra alocado pelo usuário
description: Suporte de amostra alocado pelo usuário
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- SDK do Windows Media Format, suporte de exemplo alocado pelo usuário
- ASF (Advanced Systems Format), suporte de amostra alocado pelo usuário
- ASF (formato de sistemas avançados), suporte de amostra alocado pelo usuário
- suporte de amostra alocado pelo usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80d6a0d9a7e19b46940093fc370bd2c8c70590d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005277"
---
# <a name="user-allocated-sample-support"></a>Suporte de amostra alocado pelo usuário

Em circunstâncias normais, o objeto leitor e o objeto leitor síncrono criam um novo objeto de buffer para cada amostra entregue ao seu aplicativo. Isso ocorre porque o objeto de leitura não tem como saber o que o seu aplicativo faz com os exemplos depois de obtê-los. Embora muitos aplicativos leiam amostras apenas para processá-los imediatamente, alguns aplicativos podem precisar manter amostras por um longo tempo. O objeto de leitura não pode, portanto, reutilizar qualquer um dos buffers que ele aloca; Ele os entrega para seu aplicativo, que então tem controle sobre eles.

O problema dessa abordagem é que um arquivo pode conter uma grande quantidade de amostras. Se cada um deles exigir que um novo objeto de buffer seja criado, muito tempo de processador será desperdiçado alocando e liberando memória. Em aplicativos com detecção de tempo, como media players, essa sobrecarga pode ser muito prejudicial para o desempenho.

Para aliviar os problemas de desempenho de amostras alocadas pelo leitor, o leitor e o leitor síncrono oferecem suporte a exemplos alocados pelo usuário. Para usar exemplos alocados por seu aplicativo, o objeto de leitura faz chamadas para um método de retorno de chamada de alocação de exemplo que você implementa. A lógica usada pelo retorno de chamada para entregar buffers ao objeto de leitura depende inteiramente de você. Você pode usar um pool de buffers para todo o arquivo ou usar vários pools de buffers, um para cada saída ou fluxo ou qualquer outro esquema que funcione para seu aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Alocando buffers para leitura de arquivo**](allocating-buffers-for-file-reading.md)
</dt> <dt>

[**Recursos de leitura de arquivo**](file-reading-features.md)
</dt> </dl>

 

 




