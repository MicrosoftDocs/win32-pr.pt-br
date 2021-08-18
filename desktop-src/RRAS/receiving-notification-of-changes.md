---
title: Recebendo notificação de alterações
description: Muitos clientes podem atualizar simultaneamente a tabela de roteamento e os clientes devem ser notificados quando ocorrem alterações nas informações de roteamento.
ms.assetid: d42e16e2-32b2-4178-967b-e937730b3cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6eddc92404acb921b31bab22736561cbbc83e4c1c641da80a8ff95352e52f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788706"
---
# <a name="receiving-notification-of-changes"></a>Recebendo notificação de alterações

Muitos clientes podem atualizar simultaneamente a tabela de roteamento e os clientes devem ser notificados quando ocorrem alterações nas informações de roteamento. Por exemplo, um cliente que não é notificado sobre as alterações de outro cliente na tabela de roteamento pode anunciar informações de rota desatualizadas. Isso pode ser impedido por clientes de programação de se registrarem no gerenciador de tabelas de roteamento para serem notificados sobre alterações na tabela de roteamento. O gerenciador de tabela de roteamento envia notificações de alterações a todos os clientes que se registram para recebê-las.

A notificação de alteração se aplica somente aos destinos. Não é possível consultar o gerenciador de tabelas de roteamento em busca de alterações em uma rota específica.

Quando uma alteração é feita em uma das rotas para um destino, o gerenciador de tabela de roteamento envia uma notificação de que ocorreu uma alteração. Essa notificação só vai para os clientes que se registraram no gerenciador de tabela de roteamento para o tipo de alteração que ocorreu. Todas as alterações nas informações de roteamento no gerenciador de tabela de roteamento ocorrem em uma ou mais exibições e as mensagens de notificação de alteração podem ser solicitadas em qualquer subconjunto de exibições com suporte.

Atualmente, há três tipos de notificações de alteração para as quais um cliente pode se registrar:

-   Notificação de qualquer alteração nas rotas para o destino. Essa solicitação é feita usando o sinalizador RTM \_ CHANGE \_ TYPE \_ ALL.
-   Notificação se a melhor rota para o destino mudar ou qualquer uma das seguintes informações para as melhores alterações de rota atuais:

    -   Preferência
    -   Próximos saltos
    -   Sinalizadores de rota

    Essa solicitação é feita usando o sinalizador RTM \_ CHANGE \_ TYPE \_ BEST.

-   Notificação de todas as alterações do tipo RTM CHANGE TYPE BEST, exceto alterações em sinalizadores de não encaminhamento \_ \_ na melhor \_ rota. Por exemplo, o gerenciador de roteador aguarda alterações desse tipo na exibição unicast e atualiza as informações no encaminhador unicast. Essa solicitação é feita usando o sinalizador RTM \_ CHANGE \_ TYPE \_ FORWARDING.

As solicitações de notificações de alterações também podem ser restritas a um subconjunto de destinos registrando-se para notificações de alterações somente para destinos "marcados". O cliente pode marcar um destino para notificação de alteração chamando [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification).

Quando ocorre uma alteração, o gerenciador de tabela de roteamento verifica se há clientes que devem ser notificados sobre essa alteração. Um cliente deverá ser notificado de uma alteração se todas as seguintes condições são atendidas:

-   O tipo de alteração que ocorreu é um tipo para o qual o cliente se registrou para notificação
-   Alterações em um destino marcado pelo cliente ocorreram ou em qualquer destino, se o cliente solicitou alterações para todos os destinos
-   O cliente solicitou notificação de alteração para a exibição em que essa alteração ocorreu

Se a alteração atender a todos os critérios acima, a alteração será armazenada em cache e o cliente será notificado.

A notificação não especifica quais são as alterações reais, apenas que elas ocorreram. O cliente deve recuperar as alterações chamando [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) usando o handle de notificação que foi obtido de uma chamada anterior para [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification).

 

 




