---
description: A API do Peer Identity Manager permite criar, enumerar e manipular identidades de pares em um aplicativo par.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: Sobre o Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d062f7324bb949c657b7687b533058cb9e74d3102eea1e484284453d3ff7f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579916"
---
# <a name="about-identity-manager"></a>Sobre o Identity Manager

A API do Peer Identity Manager permite criar, enumerar e manipular identidades de pares em um aplicativo par. Você pode usar as identidades de par criadas usando essa API como entrada para as APIs do provedor de namespace DE PNRP (Peer Grouping and Peer Name Resolution Protocol).

## <a name="peer-identity-manager-best-practices"></a>Práticas recomendadas do Peer Identity Manager

Cada usuário deve ter algumas identidades de par que podem ser usadas para as atividades de par. Por exemplo, um usuário pode ter duas identidades de par para trabalho e saúde.

Um aplicativo par bem projetado permite que um usuário selecione uma identidade de par a ser usada. Um usuário poderá criar uma nova identidade de par se nenhuma das identidades de par existentes for apropriada para usar com um aplicativo.

Um aplicativo par bem projetado também controla o número de identidades que ele cria. Se um aplicativo criar uma identidade de par temporária, o aplicativo deverá excluir a identidade par quando a identidade não for necessária. Se um aplicativo não executar essa manutenção, o Peer Identity Manager poderá não conseguir criar identidades de par até que algumas identidades de par sejam removidas.

 

 



