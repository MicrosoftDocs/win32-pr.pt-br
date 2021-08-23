---
description: A ação StopServices interrompe os serviços do sistema. Essa ação consulta a tabela ServiceControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Ação StopServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee0082d1588c3a1486b51bd4f06869374e1f6babfa71d309d65512e1ff1b0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627376"
---
# <a name="stopservices-action"></a>Ação StopServices

A ação StopServices interrompe os serviços do sistema. Essa ação consulta a [tabela ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

As ações de serviços devem ser usadas na seguinte sequência:

-   StopServices
-   [DeleteServices](deleteservices-action.md)

Qualquer uma das seguintes ações:

-   [InstallFiles](installfiles-action.md)
-   [RemoveFiles](removefiles-action.md)
-   [DuplicateFiles](duplicatefiles-action.md)
-   [MoveFiles](movefiles-action.md)
-   [PatchFiles](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [InstallServices](installservices-action.md)
-   [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação |
|-------|----------------------------|
| \[1\] | Nome de exibição do serviço.      |
| \[2\] | Nome do serviço.              |



 

## <a name="remarks"></a>Comentários

Essa ação exige que o usuário seja um administrador ou tenha privilégios elevados com permissão para controlar serviços ou que o aplicativo seja parte de uma instalação gerenciada.

 

 



