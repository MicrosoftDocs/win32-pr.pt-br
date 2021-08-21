---
title: Removendo membros de grupos em um domínio
description: Você pode remover usuários, grupos ou contatos de grupos.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- grupos do AD , removendo membros de grupos em um domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f282cf2938996059ad13fe74bc9818e984967d1c8f3a4dbfffae7b505cbe1b9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025154"
---
# <a name="removing-members-from-groups-in-a-domain"></a>Removendo membros de grupos em um domínio

Você pode remover usuários, grupos ou contatos de grupos. O **atributo** membro do objeto **de** grupo contém todos os membros diretos do grupo.

A maneira mais simples de remover um membro de um grupo é chamar o método [**IADsGroup.Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) na interface [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) do objeto de grupo do que você deseja remover membros.

 

 