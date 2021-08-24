---
description: A ação InstallServices registra um serviço para o sistema. Essa ação consulta a tabela ServiceInstall.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Ação InstallServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e37ea0a80050d6e9ab624ff878a352f96bbc0854fd64d6a1f563f277f1ea6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787016"
---
# <a name="installservices-action"></a>Ação InstallServices

A ação InstallServices registra um serviço para o sistema. Essa ação consulta a tabela [ServiceInstall](serviceinstall-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação de serviços deve ser usada na sequência a seguir.

[StopServices](stopservices-action.md)

[DeleteServices](deleteservices-action.md)

Qualquer uma das seguintes ações: [ações InstallFiles,](installfiles-action.md) [RemoveFiles,](removefiles-action.md) [DuplicateFiles,](duplicatefiles-action.md) [MoveFiles,](movefiles-action.md) [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles.](removeduplicatefiles-action.md)

InstallServices

[StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há mensagens ActionData.

## <a name="remarks"></a>Comentários

Essa ação exige que o usuário seja um administrador ou tenha privilégios elevados com permissão para instalar serviços ou que o aplicativo seja parte de uma instalação gerenciada.

 

 



