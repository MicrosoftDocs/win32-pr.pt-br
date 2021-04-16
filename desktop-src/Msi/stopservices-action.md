---
description: A ação StopServices interrompe os serviços do sistema. Esta ação consulta a tabela de UserControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Ação StopServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb271b99c434a1ac54ab9744697b991e9e1fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758760"
---
# <a name="stopservices-action"></a>Ação StopServices

A ação StopServices interrompe os serviços do sistema. Esta ação consulta a [tabela de UserControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

As ações de serviços devem ser usadas na seguinte sequência:

-   Pararservices
-   [Excluirservices](deleteservices-action.md)

Qualquer uma das seguintes ações:

-   [InstallFiles](installfiles-action.md)
-   [Removes](removefiles-action.md)
-   [DuplicateFiles](duplicatefiles-action.md)
-   [MoveFile](movefiles-action.md)
-   [PatchFiles](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [Instalarservices](installservices-action.md)
-   [Iniciarservices](startservices-action.md)

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação |
|-------|----------------------------|
| \[1\] | Nome de exibição do serviço.      |
| \[2\] | Nome do serviço.              |



 

## <a name="remarks"></a>Comentários

Essa ação requer que o usuário seja um administrador ou tenha privilégios elevados com permissão para controlar serviços ou que o aplicativo faça parte de uma instalação gerenciada.

 

 



