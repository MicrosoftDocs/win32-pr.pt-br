---
title: Enumerando Membros em um grupo
description: Saiba mais sobre como enumerar Membros em um grupo de Azure Active Directory. Os membros de um grupo são armazenados em um atributo com vários valores chamado membro.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Enumerando Membros em um grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916b988cd26ee4df59eaf27cc5ffd690bca1458a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407419"
---
# <a name="enumerating-members-in-a-group"></a>Enumerando Membros em um grupo

Os membros de um grupo são armazenados em um atributo com vários valores chamado **membro**. Para grupos com uma associação de tamanho pequeno e médio, use o método [**IADs. Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) para obter um ponteiro para um objeto [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) que contém a lista de todos os membros. Em seguida, use o [**IADsMembers:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) para obter um objeto Enumerator que você pode usar para enumerar os membros.

Se a associação de grupo prevista for 1000 ou mais membros, use a variação para recuperar os usuários um intervalo por vez. Para obter mais informações sobre como usar variando para enumerar Membros, consulte [enumerando grupos que contêm muitos membros](enumerating-groups-that-contain-many-members.md).

 

 