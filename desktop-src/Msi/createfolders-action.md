---
description: A ação CreateFolders cria pastas vazias para componentes que estão definidos para serem instalados.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Ação CreateFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61182143488627c4724e470bf7f5158ed524cb4bc344c972c6744d14f773f6cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105266"
---
# <a name="createfolders-action"></a>Ação CreateFolders

A ação CreateFolders cria pastas vazias para componentes que estão definidos para serem instalados. O instalador cria pastas para componentes que são executados localmente e executados da origem. As pastas recém-criadas são registradas com o identificador de componente apropriado.

A ação CreateFolders consulta a [tabela CreateFolder e](createfolder-table.md) a [tabela Component](component-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação CreateFolders deve ser executada antes da [ação InstallFiles](installfiles-action.md) ou antes de qualquer ação que adiciona arquivos a pastas.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição da descrição dos dados de ação |
|-------|----------------------------------------|
| \[1\] | Identificador de diretório da pasta.        |



 

## <a name="remarks"></a>Comentários

O instalador não remove automaticamente as pastas criadas pela ação CreateFolders durante uma desinstalação do aplicativo. O instalador só removerá pastas se a [ação RemoveFolders](removefolders-action.md) for incluída na sequência de ação.

 

 



