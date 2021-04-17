---
description: A ação RegisterTypeLibraries registra bibliotecas de tipos com o sistema. Essa ação é aplicada a cada arquivo referenciado na tabela TypeLib que está agendada para instalação.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Ação RegisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754347"
---
# <a name="registertypelibraries-action"></a>Ação RegisterTypeLibraries

A ação RegisterTypeLibraries registra bibliotecas de tipos com o sistema. Essa ação é aplicada a cada arquivo referenciado na [tabela Typelib](typelib-table.md) que está agendada para instalação.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RegisterTypeLibraries deve vir após a ação [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                   |
|-------|----------------------------------------------|
| \[1\] | [GUID](guid.md) da biblioteca de tipos registrada. |



 

## <a name="remarks"></a>Comentários

A ação RegisterTypeLibraries requer que o idioma da biblioteca de tipos seja criado corretamente no campo idioma da tabela TypeLib. A criação incorreta do campo de idioma pode fazer com que o instalador falhe ao registrar uma biblioteca de tipos válida de outra forma.

 

 



