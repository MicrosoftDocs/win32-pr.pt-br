---
title: Dados arbitrários personalizados Fluxos
description: Dados arbitrários personalizados Fluxos
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows SDK de Formato de Mídia, fluxos de dados arbitrários personalizados
- ASF (Advanced Systems Format), fluxos de dados arbitrários personalizados
- ASF (Formato de Sistemas Avançados), fluxos de dados arbitrários personalizados
- Windows SDK de Formato de Mídia, fluxos
- ASF (Advanced Systems Format), streams
- ASF (Formato de Sistemas Avançados), fluxos
- fluxos de dados arbitrários personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde40c7283620aba9c0bbdd0a1b376538ce7e4f22ac12e9fcdfe78d75195a516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027934"
---
# <a name="custom-arbitrary-data-streams"></a>Dados arbitrários personalizados Fluxos

Você pode criar um fluxo em um arquivo ASF para conter qualquer tipo de dados. Se nenhum dos tipos de fluxo com suporte atende às suas necessidades, você deve usar um fluxo de dados arbitrário. O objeto writer trata um fluxo de dados arbitrário da mesma forma que faz com qualquer fluxo descompactado; os exemplos são pacotes e combinados com os exemplos de outros fluxos na seção de dados do arquivo. É claro que apenas um aplicativo de leitura que foi especificamente programado para lidar com seu tipo arbitrário poderá lidar com os dados depois que eles são entregues pelo objeto de leitura.

Um uso comum de fluxos de dados arbitrários é para dados de mídia codificados usando um codec de terceiros. Como os objetos desse SDK não interagem diretamente com codecs de terceiros, seu aplicativo de escrita deve processar os exemplos com a parte de codificação do codec e passar os exemplos compactados para o autor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Dados arbitrários Fluxos**](arbitrary-streams.md)
</dt> <dt>

[**Configurando o recurso arbitrário personalizado Fluxos**](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




