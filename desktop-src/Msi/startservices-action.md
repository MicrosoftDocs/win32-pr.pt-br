---
description: A ação Startservices inicia os serviços do sistema. Esta ação consulta a tabela de UserControl.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: Ação de iniciarservices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ff7b927eb4bc157530cebe9767ef7a434d92f0b72f9e6c799b02a2969f5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627526"
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

 

 



