---
title: Monikers assíncronos
description: Monikers assíncronos
ms.assetid: 24c50f7b-f085-4086-aa44-81e5cab011cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19323af3a972a2b83a290176a4b26fb79382da0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105814560"
---
# <a name="asynchronous-monikers"></a>Monikers assíncronos

A arquitetura de moniker do OLE fornece um modelo de programação consistente e extensível para trabalhar com objetos da Internet, fornecendo métodos para analisar nomes, representando URLs (localizadores de recursos universal) como nomes imprimíveis e localizar e associar aos objetos representados por cadeias de caracteres de URL. (Consulte também [moniker de URL](url-monikers.md).) No entanto, os monikers OLE padrão (notadamente, item, File e Pointer moniker), no entanto, são inadequados para a Internet porque são síncronos, retornando um ponteiro para um objeto ou seu armazenamento somente no momento em que todos os dados estão disponíveis. Dependendo da quantidade de dados a serem baixados, a associação síncrona pode vincular a interface do usuário do cliente por períodos prolongados.

A Internet requer novas abordagens para o design do aplicativo. Os aplicativos devem ser capazes de executar todas as operações de rede caras de forma assíncrona para evitar a paralisação da interface do usuário. Um aplicativo deve ser capaz de disparar uma operação e receber uma notificação em conclusão completa ou parcial. Nesse ponto, o aplicativo deve ter a opção de prosseguir com a próxima etapa da operação ou fornecer informações adicionais, conforme necessário. Como o download prossegue, um aplicativo também deve ser capaz de fornecer aos usuários informações de progresso e a oportunidade de cancelar a operação a qualquer momento.

Os monikers assíncronos fornecem esses recursos, bem como vários níveis de comportamento de vinculação assíncrona, enquanto fornecem compatibilidade com versões anteriores para aplicativos que não sabem ou não exigem comportamento assíncrono. Outra tecnologia OLE, armazenamento assíncrono, funciona com monikers assíncronos para fornecer download assíncrono do estado persistente de um objeto de Internet. O moniker assíncrono dispara a operação de ligação e configura os componentes necessários, incluindo objetos de armazenamento e fluxo, objetos de matriz de bytes e coletores de notificação. Depois que os componentes estiverem conectados, o moniker ficará fora do caminho e o restante da ligação será executado principalmente entre os componentes que implementam os componentes de armazenamento assíncronos e o objeto.

Para mais informações, consulte os seguintes tópicos:

-   [Monikers assíncronos e síncronos](./asynchronous-vs.-synchronous-monikers.md)
-   [Associação assíncrona e síncrona](./asynchronous-vs.-synchronous-binding.md)
-   [Armazenamento assíncrono e síncrono](./asynchronous-vs.-synchronous-storage.md)
-   [Modelo de pull de dados e modelo de Data-Push](./data-pull-model-vs.-data-push-model.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Identificadores de URL](url-monikers.md)
</dt> </dl>

 

 