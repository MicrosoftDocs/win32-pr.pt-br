---
title: Para gerenciar a latência do gravador
description: Para gerenciar a latência do gravador
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Formato de sistema avançado (ASF), gerenciamento de latência de gravador
- ASF (formato de sistemas avançados), gerenciamento de latência de gravador
- ASF (Advanced Systems Format), latência do gravador
- ASF (formato de sistemas avançados), latência do gravador
- latência do gravador
- latência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0adb18814cc8153ae81ed9517834d62345f18b61f51de6aacd38e9028699331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845476"
---
# <a name="to-manage-writer-latency"></a>Para gerenciar a latência do gravador

Leva tempo para o gravador processar exemplos. A quantidade de tempo entre passar um exemplo de entrada e a gravação de um exemplo de saída é chamada de latência do gravador. Vários fatores contribuem para a latência do gravador e você pode reduzi-lo de várias maneiras.

O fator mais óbvio envolvido na latência do gravador é o tempo necessário para compactar um exemplo. Na maioria das circunstâncias, você terá pouco ou nenhum controle sobre isso. Se a largura de banda não for uma grande preocupação, você poderá reduzir a latência usando menos compactação. É claro que você pode obter a menor latência passando exemplos que já foram compactados.

O próximo fator, e um sobre o qual você geralmente tem controle, é a ordem em que os exemplos são passados para o leitor. Você pode obter uma latência melhor passando amostras em ordem de tempo de apresentação e garantindo que os exemplos de entrada sejam bem sincronizados entre todos os fluxos de entrada. Quanto maior a discrepância nos tempos de apresentação entre os exemplos de fluxos diferentes, mais latência será resultado. Você pode definir um máximo para a discrepância entre os exemplos de entrada chamando [**IWMWriterAdvanced:: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




