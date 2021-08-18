---
description: Filtros de senha
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Filtros de senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5771fce0e8cbb2826bcf79344e2813587db6dcedc831d7e879b42ab74698b9a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893993"
---
# <a name="password-filters"></a>Filtros de senha

Os filtros de senha fornecem uma maneira de implementar a política de senha e a notificação de alteração.

Quando uma solicitação de alteração de senha é feita, a [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) chama os filtros de senha registrados no sistema. Cada filtro de senha é chamado duas vezes: primeiro para validar a nova senha e, depois que todos os filtros tiverem validado a nova senha, para notificar os filtros de que a alteração foi feita. A ilustração a seguir mostra este processo.

![solicitação de alteração de senha](images/pswdfilte.png)

A notificação de alteração de senha é usada para sincronizar as alterações de senha para bancos de dados de conta externa.

Os filtros de senha são usados para impor a política de senha. Os filtros validam novas senhas e indicam se a nova senha está em conformidade com a política de senha implementada.

Para obter uma visão geral do uso de filtros de senha, consulte [usando filtros de senha](using-password-filters.md).

Para obter uma lista de funções de filtro de senha, consulte [funções de filtro de senha](management-functions.md).

Os tópicos a seguir fornecem mais informações sobre filtros de senha:

-   [Considerações sobre programação de filtro de senha](password-filter-programming-considerations.md)
-   [Imposição de senha forte e Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)

 

 
