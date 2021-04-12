---
description: A ação IsolateComponents instala uma cópia de um componente (normalmente uma DLL compartilhada) em um local privado para uso por um aplicativo específico (normalmente um. exe).
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Ação IsolateComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297445"
---
# <a name="isolatecomponents-action"></a>Ação IsolateComponents

A ação IsolateComponents instala uma cópia de um componente (normalmente uma DLL compartilhada) em um local privado para uso por um aplicativo específico (normalmente um. exe). Isso isola o aplicativo de outras cópias do componente que podem ser instaladas em um local compartilhado no computador. Para obter mais informações, consulte [componentes isolados](isolated-components.md).

A ação refere-se a cada registro da [tabela IsolatedComponent](isolatedcomponent-table.md) e associa os arquivos do componente listado no \_ campo compartilhado do componente ao componente listado no \_ campo aplicativo de componente. O instalador instala os arquivos do componente \_ compartilhado no mesmo diretório que o aplicativo de componente \_ . O instalador gera um arquivo nesse diretório, com comprimento de zero bytes, com o nome do nome de arquivo curto para o aplicativo de componente \_ (normalmente, esse é o mesmo nome de arquivo que o. exe) acrescentado com. local. A ação IsolatedComponent não afeta a instalação do aplicativo de componente \_ . A desinstalação do \_ aplicativo de componente também remove os \_ arquivos compartilhados do componente e o arquivo. local do diretório.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação IsolateComponents pode ser usada somente na [tabela InstallUISequence](installuisequence-table.md) e na [tabela InstallExecuteSequence](installexecutesequence-table.md). Essa ação deve vir após a [ação CostInitialize](costinitialize-action.md) e antes da [ação CostFinalize](costfinalize-action.md).

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

Se a coluna condição da ação IsolateComponents for avaliada como true ou for deixada em branco, o instalador isolará todos os componentes listados na [tabela IsolatedComponent](isolatedcomponent-table.md). Se a coluna Condition for avaliada como false, o instalador ignorará a tabela IsolatedComponent e compartilhará os componentes de forma usual. A propriedade [**RedirectedDllSupport**](redirecteddllsupport.md) pode ser usada para condição dessa ação. Para obter mais informações, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

 

 



