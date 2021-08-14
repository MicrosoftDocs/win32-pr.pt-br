---
description: Uma ação personalizada em uma tabela de sequência de interface do usuário ou em um arquivo executável externo pode precisar do nível de interface do usuário atual da instalação.
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: Determinando o nível da interface do usuário de uma ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af88753b5ea44927ac58b13bcb4742e7992e50e1499aa04964b60b632d68ec53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947563"
---
# <a name="determining-ui-level-from-a-custom-action"></a>Determinando o nível da interface do usuário de uma ação personalizada

Uma ação personalizada em uma tabela de sequência de interface do usuário ou em um arquivo executável externo pode precisar do nível de interface do usuário atual da instalação. Por exemplo, uma ação personalizada que tem uma caixa de diálogo só deverá exibir a caixa de diálogo quando o nível da interface do usuário for interface do usuário completa ou interface do usuário reduzida, ela não deverá exibir a caixa de diálogo se o nível da interface do usuário for UI Básica ou Nenhum. Você deve usar a [**propriedade UILevel**](uilevel.md) para determinar o nível atual da interface do usuário. Você não pode [**chamar MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) de uma ação personalizada e não é possível alterar a propriedade de nível de interface do usuário de dentro de uma ação personalizada.

É recomendável que ações personalizadas não usem o nível da interface do usuário como uma condição para enviar mensagens de erro ao instalador porque isso pode interferir no registro em log e em mensagens externas.

 

 



