---
title: Recebendo notificação de alterações
description: Muitos clientes podem atualizar simultaneamente a tabela de roteamento e os clientes devem ser notificados quando ocorrem alterações nas informações de roteamento.
ms.assetid: d42e16e2-32b2-4178-967b-e937730b3cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacd8d1d0329cf29be82a890be30b602b9330249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363886"
---
# <a name="receiving-notification-of-changes"></a>Recebendo notificação de alterações

Muitos clientes podem atualizar simultaneamente a tabela de roteamento e os clientes devem ser notificados quando ocorrem alterações nas informações de roteamento. Por exemplo, um cliente que não é notificado sobre as alterações de outro cliente na tabela de roteamento poderia anunciar informações de rota desatualizadas. Isso pode ser evitado pela programação de clientes para se registrarem com o Gerenciador de tabela de roteamento para serem notificados sobre alterações na tabela de roteamento. O Gerenciador de tabela de roteamento envia notificações de alterações a todos os clientes que se registram para recebê-las.

A notificação de alteração se aplica somente a destinos. Não é possível consultar o Gerenciador de tabela de roteamento para alterações em uma rota específica.

Quando uma alteração é feita em uma das rotas para um destino, o Gerenciador de tabela de roteamento envia uma notificação de que ocorreu uma alteração. Essa notificação vai apenas para os clientes que se registraram com o Gerenciador de tabela de roteamento para o tipo de alteração que ocorreu. Todas as alterações nas informações de roteamento no Gerenciador de tabela de roteamento ocorrem em um ou mais modos de exibição e as mensagens de notificação de alteração podem ser solicitadas em qualquer subconjunto de exibições com suporte.

Atualmente, há três tipos de notificações de alteração para os quais um cliente pode se registrar:

-   Notificação de qualquer alteração nas rotas para o destino. Essa solicitação é feita usando o \_ sinalizador alterar tipo de alteração RTM \_ \_ .
-   Notificação se a melhor rota para o destino for alterada ou qualquer uma das seguintes informações para as melhores alterações de rota atuais:

    -   Preferência
    -   Próximos saltos
    -   Sinalizadores de rota

    Essa solicitação é feita usando o \_ sinalizador do \_ melhor tipo de alteração RTM \_ .

-   Notificação de todas as alterações do tipo tipo de \_ alteração RTM \_ \_ melhor, exceto alterações em sinalizadores de não encaminhamento na melhor rota. Por exemplo, o Gerenciador de roteador aguarda as alterações desse tipo na exibição unicast e atualiza as informações no encaminhador unicast. Essa solicitação é feita usando o \_ sinalizador de \_ encaminhamento do tipo de alteração RTM \_ .

As solicitações de notificações de alterações também podem ser restritas a um subconjunto de destinos registrando-se para notificações de alterações apenas em destinos "marcados". O cliente pode marcar um destino para a notificação de alteração chamando [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification).

Quando ocorre uma alteração, o Gerenciador de tabela de roteamento verifica se há clientes que devem ser notificados sobre essa alteração. Um cliente deve ser notificado sobre uma alteração se todas as condições a seguir forem atendidas:

-   O tipo de alteração que ocorreu é um tipo para o qual o cliente registrou para notificação
-   As alterações em um destino que o cliente marcou ter ocorrido ou qualquer destino, se o cliente tiver solicitado alterações para todos os destinos
-   O cliente solicitou notificação de alteração para a exibição na qual essa alteração ocorreu

Se a alteração atender a todos os critérios acima, a alteração será armazenada em cache e o cliente será notificado.

A notificação não especifica quais são as alterações reais, apenas se elas ocorreram. O cliente deve recuperar as alterações chamando [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) usando o identificador de notificação que foi obtido de uma chamada anterior para [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification).

 

 




