---
description: A ação createfolders cria pastas vazias para componentes que estão definidos para serem instalados.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Ação createfolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780962"
---
# <a name="createfolders-action"></a>Ação createfolders

A ação createfolders cria pastas vazias para componentes que estão definidos para serem instalados. O instalador cria pastas para componentes que são executados localmente e executados a partir da origem. As pastas recém-criadas são registradas com o identificador de componente apropriado.

A ação createfolders consulta a [tabela CreateFolder](createfolder-table.md) e a [tabela de componentes](component-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação createfolders deve ser executada antes da ação [InstallFiles](installfiles-action.md) ou antes de qualquer ação que adicione arquivos a pastas.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição da descrição dos dados da ação |
|-------|----------------------------------------|
| \[1\] | Identificador de diretório da pasta.        |



 

## <a name="remarks"></a>Comentários

O instalador não remove automaticamente as pastas criadas pela ação createfolders durante uma desinstalação do aplicativo. O instalador só removerá pastas se a [ação RemoveFolders](removefolders-action.md) estiver incluída na sequência de ação.

 

 



