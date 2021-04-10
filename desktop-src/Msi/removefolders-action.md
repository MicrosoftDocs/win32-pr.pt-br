---
description: A ação RemoveFolders remove todas as pastas vinculadas aos componentes definidos para serem removidas ou executadas da origem. Essas pastas serão removidas somente se estiverem vazias. Se uma pasta for removida, ela não será registrada com o identificador de componente apropriado.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: Ação RemoveFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69648fbae333f0e7b989f2e989f0982d49736317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170423"
---
# <a name="removefolders-action"></a>Ação RemoveFolders

A ação RemoveFolders remove todas as pastas vinculadas aos componentes definidos para serem removidas ou executadas da origem. Essas pastas serão removidas somente se estiverem vazias. Se uma pasta for removida, ela não será registrada com o identificador de componente apropriado.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RemoveFolders deve vir [após a ação](removefiles-action.md) removidas ou qualquer ação que possa remover arquivos de pastas.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação    |
|-------|-------------------------------|
| \[1\] | Identificador da pasta removida. |



 

## <a name="remarks"></a>Comentários

O instalador não remove automaticamente as pastas criadas pela [ação Createfolders](createfolders-action.md) durante uma desinstalação do aplicativo. O instalador deve ser instruído para remover essas pastas, criando a ação RemoveFolders na sequência de ação.

Para especificar o nome e o local da pasta, use a \_ coluna Directory da [tabela CreateFolder](createfolder-table.md). Supõe-se que cada nome de pasta na tabela CreateFolder seja uma propriedade que define o local da pasta.

Para especificar o componente que possui a pasta, use a coluna ComponentID da [tabela de componentes](component-table.md).

 

 



