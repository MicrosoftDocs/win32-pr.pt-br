---
title: Determinando a associação de um usuário ou grupo em um grupo
description: O método IADs. IsMember pode ser usado para determinar se um objeto é membro de um grupo.
ms.assetid: c7168781-4ae4-4ce3-8d8a-2eefc7def62b
ms.tgt_platform: multiple
keywords:
- Determinando a associação de um usuário ou grupo em um AD do grupo
- grupos de anúncios, determinando a associação de um usuário ou grupo em um grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b520146079fdfaa5fa1adc99975b3b25d2e78c05
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007327"
---
# <a name="determining-a-users-or-groups-membership-in-a-group"></a>Determinando a associação de um usuário ou grupo em um grupo

O método [**IADs. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) pode ser usado para determinar se um objeto é membro de um grupo. Esse método retornará **true** se o objeto especificado for um membro direto do grupo, ou seja, a propriedade de membro do grupo contiver o objeto especificado.

Um grupo pode conter outros grupos. O método [**IADs. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) não verifica recursivamente os membros dos grupos em sua Propriedade Member, os grupos dentro desses grupos e assim por diante. Para verificar recursivamente se um objeto é membro de um grupo, enumere os grupos na Propriedade do membro, verifique os membros desses grupos para ver se o objeto é um membro e se esses grupos contêm outros grupos, verifique seus membros e assim por diante.

> [!Note]  
> Como os grupos podem ser aninhados, a associação de grupo pode ter loops. Qualquer script que enumere muitos grupos deve manter uma lista interna de grupos para encerrar a recursão se um grupo já tiver sido visitado.

 

 

 