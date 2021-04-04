---
title: Enumerando Membros em um grupo
description: Os membros de um grupo são armazenados em um atributo com vários valores chamado membro.
ms.assetid: 28cafdbe-e599-4b1d-a384-264f41d81c79
ms.tgt_platform: multiple
keywords:
- Enumerando Membros em um grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2d051999bf8efeadb0c5a8899b31f813b8bf42
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084449"
---
# <a name="enumerating-members-in-a-group"></a>Enumerando Membros em um grupo

Os membros de um grupo são armazenados em um atributo com vários valores chamado **membro**. Para grupos com uma associação de tamanho pequeno e médio, use o método [**IADs. Members**](/windows/desktop/api/iads/nf-iads-iadsgroup-members) para obter um ponteiro para um objeto [**IADsMembers**](/windows/desktop/api/iads/nn-iads-iadsmembers) que contém a lista de todos os membros. Em seguida, use o [**IADsMembers:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsmembers-get__newenum) para obter um objeto Enumerator que você pode usar para enumerar os membros.

Se a associação de grupo prevista for 1000 ou mais membros, use a variação para recuperar os usuários um intervalo por vez. Para obter mais informações sobre como usar variando para enumerar Membros, consulte [enumerando grupos que contêm muitos membros](enumerating-groups-that-contain-many-members.md).

 

 