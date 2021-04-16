---
description: A ação Startservices inicia os serviços do sistema. Esta ação consulta a tabela de UserControl.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: Ação de iniciarservices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c150a8970c5852d9cfc53581290e792c00b628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779622"
---
# <a name="startservices-action"></a>Ação de iniciarservices

A ação Startservices inicia os serviços do sistema. Esta ação consulta a [tabela de UserControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

As ações de serviços devem ser usadas na seguinte sequência:

-   [Pararservices](stopservices-action.md)
-   [Excluirservices](deleteservices-action.md)

Qualquer uma das seguintes ações:

-   [InstallFiles](installfiles-action.md)
-   [Removes](removefiles-action.md)
-   [DuplicateFiles](duplicatefiles-action.md)
-   [MoveFile](movefiles-action.md)
-   [PatchFiles](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [Instalarservices](installservices-action.md)
-   Iniciarservices

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação |
|-------|----------------------------|
| \[1\] | Nome de exibição do serviço.      |
| \[2\] | Nome do serviço.              |



 

## <a name="remarks"></a>Comentários

Essa ação requer que o usuário seja um administrador ou tenha privilégios elevados com permissão para controlar serviços ou que o aplicativo faça parte de uma instalação gerenciada.

 

 



