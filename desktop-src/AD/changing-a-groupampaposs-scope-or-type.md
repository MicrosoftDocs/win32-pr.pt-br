---
title: Alterando o escopo ou tipo de um grupo
description: Este tópico mostra como alterar o escopo ou o tipo de um grupo em domínios de modo nativo.
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- grupos de anúncios, alterando o escopo ou tipo de um grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634804"
---
# <a name="changing-a-groups-scope-or-type"></a>Alterando o escopo ou tipo de um grupo

A alteração de um escopo ou tipo de grupo não é permitida em domínios de modo misto. No entanto, as seguintes conversões são permitidas em domínios de modo nativo:

Grupo global para grupo universal: isso só será permitido se o grupo global não for membro de outro grupo global.

Grupo de domínio local para grupo universal: o grupo local de domínio que está sendo convertido não pode conter outro grupo de domínio local.

Grupo universal para grupo local global ou de domínio: para conversão para grupo global, o grupo universal que está sendo convertido não pode conter usuários ou grupos globais de outro domínio. Para conversão para grupo de domínio local, o grupo universal que está sendo convertido não pode ser membro de um grupo universal ou de um grupo de domínio local de outro domínio.

No modo nativo, um tipo de grupo pode ser convertido livremente entre grupos de segurança e grupos de distribuição.

Lembre-se de que, se um grupo for usado para definir o controle de acesso, alterar o escopo ou o tipo poderá afetar as ACEs (entradas de controle de acesso) que contêm esse grupo. O sistema de segurança irá ignorar ACEs que contêm grupos que não são grupos de segurança.

 

 




