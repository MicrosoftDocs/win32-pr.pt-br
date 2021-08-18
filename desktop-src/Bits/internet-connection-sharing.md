---
title: Compartilhamento de Conexão com a Internet
description: O BITS poderá forçar uma conexão discada para redes base que usam o Compartilhamento de Conexão com a Internet da Microsoft se o Compartilhamento de Conexão estiver configurado para discar quando os computadores na rede acessarem a Internet.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8736144b74d12666c4a364ac5b644ead35f8d1ec28aa03926bb7b691c8218f3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588616"
---
# <a name="internet-connection-sharing"></a>Compartilhamento de Conexão com a Internet

O BITS poderá forçar uma conexão discada para redes base que usam o Compartilhamento de Conexão com a Internet da Microsoft se o Compartilhamento de Conexão estiver configurado para discar quando os computadores na rede acessarem a Internet. Para evitar uma conexão discar forçada, desabilite a opção Estabelecer uma conexão discável sempre que um computador em minha rede tentar acessar a opção Internet no computador host de Compartilhamento de Conexão que compartilha sua conexão com **a** Internet.

Os computadores conectados ao computador host do Compartilhamento de Conexão pressuem que tenham uma conexão de rede, portanto, o BITS tentará transferir arquivos. Se a opção de discagem estiver desabilitada no computador host e o computador host não tiver uma conexão ativa, as transferências falharão com um erro transitório. O BITS repetirá as transferências periodicamente.

 

 




