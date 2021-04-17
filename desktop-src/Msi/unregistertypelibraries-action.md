---
description: A ação UnregisterTypeLibraries cancela o registro de bibliotecas de tipos do sistema. Essa ação é aplicada a cada arquivo listado na tabela TypeLib que é disparada para ser desinstalada.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Ação UnregisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748755"
---
# <a name="unregistertypelibraries-action"></a>Ação UnregisterTypeLibraries

A ação UnregisterTypeLibraries cancela o registro de bibliotecas de tipos do sistema. Essa ação é aplicada a cada arquivo listado na tabela [TypeLib](typelib-table.md) que é disparada para ser desinstalada.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação UnregisterTypeLibraries deve vir antes da ação [RemoveFiles](removefiles-action.md) .

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                        |
|-------|---------------------------------------------------|
| \[1\] | [GUID](guid.md) de uma biblioteca de tipos não registrada. |



 

 

 



