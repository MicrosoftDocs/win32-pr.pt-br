---
description: A ação Installservices registra um serviço para o sistema. Esta ação consulta a tabela de instalação.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Ação installservices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789778"
---
# <a name="installservices-action"></a>Ação installservices

A ação Installservices registra um serviço para o sistema. Esta ação consulta a [tabela de instalação](serviceinstall-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação de serviços deve ser usada na sequência a seguir.

[Pararservices](stopservices-action.md)

[Excluirservices](deleteservices-action.md)

Qualquer uma das seguintes ações: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles](removeduplicatefiles-action.md) ações.

Instalarservices

[Iniciarservices](startservices-action.md)

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

Essa ação requer que o usuário seja um administrador ou tenha privilégios elevados com permissão para instalar serviços ou que o aplicativo faça parte de uma instalação gerenciada.

 

 



