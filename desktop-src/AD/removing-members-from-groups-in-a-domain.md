---
title: Removendo membros de grupos em um domínio
description: Você pode remover usuários, grupos ou contatos de grupos.
ms.assetid: 036f2882-7da9-4293-87a0-a087235b212f
ms.tgt_platform: multiple
keywords:
- grupos de anúncios, removendo membros de grupos em um domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab7600d98e75447c55fd84d783ff5263fc63bde
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640386"
---
# <a name="removing-members-from-groups-in-a-domain"></a>Removendo membros de grupos em um domínio

Você pode remover usuários, grupos ou contatos de grupos. O atributo **Member** do objeto **Group** contém todos os membros diretos do grupo.

A maneira mais simples de remover um membro de um grupo é chamar o método [**IADs. Remove**](/windows/desktop/api/iads/nf-iads-iadsgroup-remove) na interface [**IADs**](/windows/desktop/api/iads/nn-iads-iadsgroup) do objeto de grupo do qual você deseja remover membros.

 

 