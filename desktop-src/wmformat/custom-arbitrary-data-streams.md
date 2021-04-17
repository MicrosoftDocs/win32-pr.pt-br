---
title: Fluxos de dados arbitrários personalizados
description: Fluxos de dados arbitrários personalizados
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- SDK do Windows Media Format, fluxos de dados arbitrários personalizados
- ASF (Advanced Systems Format), fluxos de dados arbitrários personalizados
- ASF (formato de sistemas avançados), fluxos de dados arbitrários personalizados
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- fluxos de dados arbitrários personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105780429"
---
# <a name="custom-arbitrary-data-streams"></a>Fluxos de dados arbitrários personalizados

Você pode criar um fluxo em um arquivo ASF para conter qualquer tipo de dados. Se nenhum dos tipos de fluxo com suporte atender às suas necessidades, você deverá usar um fluxo de dados arbitrário. O objeto do gravador manipula um fluxo de dados arbitrários da mesma forma que faz qualquer fluxo descompactado; Os exemplos são incluídos em pacotes e combinados com os exemplos de outros fluxos na seção de dados do arquivo. É claro que apenas um aplicativo de leitura que tenha sido programado especificamente para lidar com seu tipo arbitrário poderá manipular os dados depois que eles forem entregues pelo objeto de leitura.

Um uso comum de fluxos de dados arbitrários é para dados de mídia codificados usando um codec de terceiros. Como os objetos desse SDK não interagem diretamente com codecs de terceiros, seu aplicativo de escrita deve processar os exemplos com a parte de codificação do codec e passar os exemplos compactados para o gravador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Fluxos arbitrários**](arbitrary-streams.md)
</dt> <dt>

[**Configurando fluxos arbitrários personalizados**](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




