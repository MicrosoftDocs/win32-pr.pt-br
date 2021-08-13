---
description: O IgnoreChange ControlEvent é publicado pelo controle DirectoryList quando a pasta selecionada é alterada de um diretório para outro no controle . Esse evento deve ser autor na tabela EventMapping.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8efc2750c4d1e2bd85f7c31348f507917f828725de95658095e964b22a110a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634454"
---
# <a name="ignorechange-controlevent"></a>IgnoreChange ControlEvent

O IgnoreChange ControlEvent é publicado pelo controle [DirectoryList](directorylist-control.md) quando a pasta selecionada é alterada de um diretório para outro no controle . Esse evento deve ser autor na [tabela EventMapping](eventmapping-table.md).

Esse ControlEvent exige que a interface do usuário seja executado no [*nível completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida ou*](r-gly.md) interface do usuário [*básica.*](b-gly.md) Para obter informações, consulte [Interface do Usuário níveis .](user-interface-levels.md)

## <a name="published-by"></a>Publicada por

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent não usa um argumento .

## <a name="action-on-subscribers"></a>Ação em Assinantes

Este ControlEvent não executa uma ação em assinantes.

## <a name="typical-use"></a>Usos comum

O [controle DirectoryCombo](directorycombo-control.md) normalmente emprega o IgnoreChange ControlEvent.

 

 



