---
title: Enumerando membros em um grupo
description: Saiba mais sobre a enumeração de membros em um Azure Active Directory grupo. Os membros de um grupo são armazenados em um atributo de vários valores chamado membro.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Enumerando membros em um grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426e2fb4fdd47f5f5b277618cb0989d8d8b06b6491d505ece20139e373ebe01f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429481"
---
# <a name="enumerating-members-in-a-group"></a>Enumerando membros em um grupo

Os membros de um grupo são armazenados em um atributo de vários valores chamado **membro**. Para grupos com uma associação de pequeno a médio porte, use o método [**IADsGroup.Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) para obter um ponteiro para um [**objeto IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) que contém a lista de todos os membros. Em seguida, [**use IADsMembers::get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) para obter um objeto enumerador que você pode usar para enumerar os membros.

Se a associação de grupo prevista for de 1000 ou mais membros, use variando para recuperar usuários um intervalo de cada vez. Para obter mais informações sobre como usar variando para enumerar membros, consulte [Enumerando grupos que contêm muitos membros](enumerating-groups-that-contain-many-members.md).

 

 