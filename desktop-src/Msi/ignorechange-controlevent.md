---
description: O IgnoreChange ControlEvent, é publicado pelo controle Directorylist quando a pasta selecionada é alterada de um diretório para outro no controle. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751653"
---
# <a name="ignorechange-controlevent"></a>IgnoreChange ControlEvent,

O IgnoreChange ControlEvent, é publicado pelo [controle directorylist](directorylist-control.md) quando a pasta selecionada é alterada de um diretório para outro no controle. Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

[Directorylist](directorylist-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent, não usa um argumento.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa uma ação nos assinantes.

## <a name="typical-use"></a>Usos comum

O [controle DirectoryCombo](directorycombo-control.md) normalmente emprega o IgnoreChange ControlEvent,.

 

 



