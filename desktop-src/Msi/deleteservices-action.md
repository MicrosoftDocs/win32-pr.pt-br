---
description: A ação DeleteServices interrompe um serviço e remove seu registro do sistema. Esta ação consulta a tabela de UserControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Ação de excluirservices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd00b9d077239402817bdf40dc10ee1de9bdbff4b52998742434933c3e9dd8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379112"
---
# <a name="deleteservices-action"></a>Ação de excluirservices

A ação DeleteServices interrompe um serviço e remove seu registro do sistema. Esta ação consulta a [tabela de UserControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

As ações de serviços devem ser usadas na seguinte sequência:

1.  [Pararservices](stopservices-action.md)
2.  Excluirservices
3.  Qualquer uma das seguintes ações: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles](removeduplicatefiles-action.md) ações.
4.  [Ação installservices](installservices-action.md)
5.  [Iniciarservices](startservices-action.md)

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação |
|-------|----------------------------|
| \[1\] | Nome de exibição do serviço.      |
| \[2\] | Nome do serviço.              |



 

## <a name="remarks"></a>Comentários

Essa ação requer que o usuário seja um administrador ou tenha privilégios elevados com permissão para excluir serviços ou que o aplicativo faça parte de uma instalação gerenciada.

 

 



