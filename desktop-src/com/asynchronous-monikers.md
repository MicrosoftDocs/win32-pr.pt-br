---
title: Monikers assíncronos
description: Monikers assíncronos
ms.assetid: 24c50f7b-f085-4086-aa44-81e5cab011cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9e9b5e427df882b7e0be84507b79c9113a46e44dad614e571a831fedecedff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859646"
---
# <a name="asynchronous-monikers"></a>Monikers assíncronos

A arquitetura de moniker OLE fornece um modelo de programação consistente e extensível para trabalhar com objetos da Internet, fornecendo métodos para analisar nomes, representando URLs (Universal Resource Locators) como nomes imprimíveis e localizando e vinculando aos objetos representados por cadeias de caracteres de URL. (Consulte também [Monikers de URL.)](url-monikers.md) Monikers OLE padrão (notavelmente, monikers de item, arquivo e ponteiro), no entanto, são inadequados para a Internet porque são síncronos, retornando um ponteiro para um objeto ou seu armazenamento apenas no momento em que todos os dados estão disponíveis. Dependendo da quantidade de dados a serem baixados, a associação de forma síncrona pode vincular a interface do usuário do cliente por períodos prolongados.

A Internet requer novas abordagens para o design do aplicativo. Os aplicativos devem ser capazes de executar todas as operações de rede caras de forma assíncrona para evitar a paralisação da interface do usuário. Um aplicativo deve ser capaz de disparar uma operação e receber notificação sobre a conclusão completa ou parcial. Nesse ponto, o aplicativo deve ter a opção de prosseguir com a próxima etapa da operação ou fornecer informações adicionais conforme necessário. Conforme o download continua, um aplicativo também deve ser capaz de fornecer aos usuários informações de progresso e a oportunidade de cancelar a operação a qualquer momento.

Os monikers assíncronos fornecem esses recursos, bem como vários níveis de comportamento de associação assíncrona, ao mesmo tempo que fornecem compatibilidade com backward para aplicativos que não têm conhecimento ou não exigem comportamento assíncrono. Outra tecnologia OLE, armazenamento assíncrono, funciona com monikers assíncronos para fornecer download assíncrono do estado persistente de um objeto da Internet. O moniker assíncrono dispara a operação de vinculação e configura os componentes necessários, incluindo objetos de armazenamento e fluxo, objetos de matriz de byte e sinks de notificação. Depois que os componentes são conectados, o moniker sai do caminho e o restante da ligação é executado principalmente entre os componentes que implementam os componentes de armazenamento assíncronos e o objeto .

Para obter mais informações, consulte estes tópicos:

-   [Monikers assíncronos e síncronos](./asynchronous-vs.-synchronous-monikers.md)
-   [Associação assíncrona e síncrona](./asynchronous-vs.-synchronous-binding.md)
-   [Assíncrono e síncrono Armazenamento](./asynchronous-vs.-synchronous-storage.md)
-   [Modelo de pull de dados e Data-Push modelo](./data-pull-model-vs.-data-push-model.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[URL Monikers](url-monikers.md)
</dt> </dl>

 

 