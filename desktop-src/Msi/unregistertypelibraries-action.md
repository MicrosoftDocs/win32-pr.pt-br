---
description: A ação UnregisterTypeLibraries cancela o registro de bibliotecas de tipos do sistema. Essa ação é aplicada a cada arquivo listado na tabela TypeLib que é disparada para ser desinstalada.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Ação UnregisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6066dbac7e63696f838375261fbb63e8348faf630a7439ec7531cdd71d4ace97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810116"
---
# <a name="unregistertypelibraries-action"></a>Ação UnregisterTypeLibraries

A ação UnregisterTypeLibraries cancela o registro de bibliotecas de tipos do sistema. Essa ação é aplicada a cada arquivo listado na tabela [TypeLib](typelib-table.md) que é disparada para ser desinstalada.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação UnregisterTypeLibraries deve vir antes da ação [RemoveFiles](removefiles-action.md) .

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                        |
|-------|---------------------------------------------------|
| \[1\] | [GUID](guid.md) de uma biblioteca de tipos não registrada. |



 

 

 



