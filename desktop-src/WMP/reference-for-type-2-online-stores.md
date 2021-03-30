---
title: Referência para lojas online do tipo 2
description: Referência para lojas online do tipo 2
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Repositórios online do Windows Media Player, referência
- lojas online, referência
- tipo 2 lojas online, referência
- referência para lojas online do tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c164ad74481030a52cd31605b29833d3bfbd3f1d
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "103640321"
---
# <a name="reference-for-type-2-online-stores"></a>Referência para lojas online do tipo 2

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O Windows Media Player 10 ou posterior fornece objetos, interfaces, propriedades e métodos que dão suporte às lojas online do tipo 2. As seções a seguir documentam esses detalhes.



| Seção                                                                                                        | Descrição                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interface IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)                                               | Fornece métodos para aumentar o DRM (gerenciamento de direitos digitais) e iniciar processos em segundo plano.                                                                              |
| [Interface IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)                                             | Fornece métodos para iniciar processos em segundo plano, para fornecer informações sobre a atividade da loja online e para fornecer um ponteiro para a interface principal do Windows Media Player. |
| [Interface IWMPSubscriptionServiceCallback](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)                               | Define um método que as lojas online usam para notificar o Windows Media Player quando um processo em segundo plano é concluído.                                                              |
| [WMPNotifySubscriptionPluginAddRemove](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove)                               | Uma função usada para notificar o Windows Media Player de que um plug-in foi instalado ou desinstalado.                                                                            |
| [Objeto downloadcollection](downloadcollection-object.md)                                                     | Fornece métodos e propriedades para gerenciar coleções de itens de download.                                                                                                    |
| [Objeto DownloadItem](downloaditem-object.md)                                                                 | Fornece métodos e propriedades relacionados a solicitações de download.                                                                                                              |
| [Objeto DownloadManager](downloadmanager-object.md)                                                           | Fornece métodos para gerenciar coleções de download.                                                                                                                            |
| [Objeto externo para lojas online do tipo 2](external-object-for-type-2-online-stores.md)                       | Fornece propriedades, métodos e um evento acessível por meio de páginas da Web da loja online.                                                                                           |
| [Enumerações para lojas online do tipo 2](enumerations-for-type-2-online-stores.md)                             | Descreve as enumerações usadas por lojas online.                                                                                                                               |
| [Convenção de trabalho BITS do Windows Media Player](windows-media-player-bits-job-convention.md)                       | Descreve uma Convenção para usar o Serviço de Transferência Inteligente em Segundo Plano (BITS).                                                                                        |
| [Chaves e entradas do registro para uma loja online tipo 2](registry-keys-and-entries-for-a-type-2-online-store.md) | Descreve as entradas do registro que um repositório online deve criar no registro no computador do usuário.                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tipo 2 lojas online**](type-2-online-stores.md)
</dt> </dl>

 

 




