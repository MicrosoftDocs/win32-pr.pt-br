---
title: Compartilhamento de Conexão com a Internet
description: O BITS pode forçar uma conexão discada para redes domésticas que usam o compartilhamento de conexão com a Internet da Microsoft se o compartilhamento de conexão estiver configurado para discar quando os computadores na rede acessarem a Internet.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f92538f0317ac1b198b69069c4041c562ce368c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635015"
---
# <a name="internet-connection-sharing"></a>Compartilhamento de Conexão com a Internet

O BITS pode forçar uma conexão discada para redes domésticas que usam o compartilhamento de conexão com a Internet da Microsoft se o compartilhamento de conexão estiver configurado para discar quando os computadores na rede acessarem a Internet. Para evitar uma conexão dial-up forçada, desabilite a opção **estabelecer uma conexão discada sempre que um computador em minha rede tentar acessar a Internet** no computador host de compartilhamento de conexão que compartilha sua conexão com a Internet.

Os computadores conectados ao computador host de compartilhamento de conexão pressupõem que eles têm uma conexão de rede, portanto, o BITS tentará transferir arquivos. Se a opção dial-up estiver desabilitada no computador host e o computador host não tiver uma conexão ativa, as transferências falharão com um erro transitório. O BITS tentará novamente as transferências periodicamente.

 

 




