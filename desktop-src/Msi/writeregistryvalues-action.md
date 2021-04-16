---
description: A ação WriteRegistryValues configura as informações de registro de um aplicativo.
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: Ação WriteRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768712"
---
# <a name="writeregistryvalues-action"></a>Ação WriteRegistryValues

A ação WriteRegistryValues configura as informações de registro de um aplicativo. As informações do registro são restringidas pela [tabela de componentes](component-table.md). Um valor de registro será gravado no registro se o componente correspondente tiver sido configurado para ser instalado localmente ou como executado da origem. Para obter mais informações, consulte [tabela do registro](registry-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A [ação InstallValidate](installvalidate-action.md) deve vir antes da ação WriteRegistryValues. Se houver uma [ação RemoveRegistryValues](removeregistryvalues-action.md), ela deverá vir antes da ação WriteRegistryValues.

Uma ação personalizada pode ser usada para adicionar linhas à [tabela do registro](registry-table.md) durante uma instalação, desinstalação ou Repair Transaction. Essas linhas não persistem na tabela do registro e as informações só estão disponíveis durante a transação atual. A ação personalizada deve, portanto, ser executada em cada instalação, desinstalação ou reparo de transação que exija as informações nessas linhas adicionais. A ação personalizada deve vir antes das ações [RemoveRegistryValues](removeregistryvalues-action.md) e WriteRegistryValues na sequência de ação.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                               |
|-------|----------------------------------------------------------|
| \[1\] | Caminho para a chave do registro do valor gravado no registro.       |
| \[2\] | Nome da cadeia de caracteres de texto formatado do valor gravado no registro. |
| \[3\] | Cadeia de texto formatada de valor gravado no registro.      |



 

 

 



