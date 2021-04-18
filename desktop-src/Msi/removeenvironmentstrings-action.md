---
description: A ação RemoveEnvironmentStrings modifica os valores das variáveis de ambiente.
ms.assetid: 024a734a-2e40-45b6-9dec-73def89a417f
title: Ação RemoveEnvironmentStrings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c958f2095d2b8562bbd7518ef691634186a9128
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792488"
---
# <a name="removeenvironmentstrings-action"></a>Ação RemoveEnvironmentStrings

A ação RemoveEnvironmentStrings modifica os valores das variáveis de ambiente.

Observe que as variáveis de ambiente não são alteradas para a instalação em andamento quando a ação [WriteEnvironmentStrings](writeenvironmentstrings-action.md) ou a ação RemoveEnvironmentStrings são executadas. No Windows 2000, essas informações são armazenadas no registro e uma mensagem é enviada para notificar o sistema sobre as alterações quando a instalação for concluída. Um novo processo ou outro processo que verifica essas mensagens usará as novas variáveis de ambiente.

O instalador executa a [ação WriteEnvironmentStrings](writeenvironmentstrings-action.md) somente durante a instalação ou reinstalação de um componente e executa a ação RemoveEnvironmentStrings somente durante a remoção de um componente.

Os valores são gravados ou removidos com base na seleção de ações e modificadores primários. Eles são descritos na seção mensagens ActionData a seguir. Observe que, dependendo da ação especificada, WriteEnvironmentStrings pode remover variáveis e RemoveEnvironmentStrings pode adicioná-las com base na criação da [tabela de ambiente](environment-table.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

A [ação InstallValidate](installvalidate-action.md) deve ser executada antes da ação RemoveEnvironmentStrings. Como a ação WriteEnvironmentStrings e a ação RemoveEnvironmentStrings nunca são aplicadas durante a instalação ou remoção de um componente, sua sequência relativa não é restrita.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                                                                                                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[1\] | Nome da variável de ambiente a ser modificada.                                                                                                                                                                               |
| \[2\] | O valor da variável de ambiente.                                                                                                                                                                                           |
| \[3\] | Esse é um campo de sinalizadores de bit que especificam a ação a ser executada. Inclua apenas um bit para uma ação principal. Pode haver mais de um bit modificador incluído neste campo. Consulte as seguintes descrições de sinalizador de bits. |



 



| Valor de bit | Descrição das ações principais                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x1       | Definido. Define o valor da variável de ambiente em todos os casos.<br/> Se esse bit for combinado com um bit de modificador de acréscimo ou de prefixo, a ação adicionará o valor a qualquer valor existente na variável.<br/> |
| 0x2       | Definido. Define o valor se a variável estiver ausente.<br/> Se esse bit for combinado com um bit de modificador de acréscimo ou de prefixo, a ação adicionará o valor a qualquer valor existente na variável.<br/>                |
| 0x4       | Remover. Remove o valor da variável.<br/> Se esse bit for combinado com um bit de modificador de acréscimo ou de prefixo, o valor será removido da cadeia de caracteres existente, se o valor existir.<br/>               |



 



| Valor de bit  | Descrição do modificador                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x20000000 | Se esse bit for definido, as ações serão aplicadas às variáveis de ambiente da máquina.<br/> Se esse bit não estiver definido, as ações serão aplicadas às variáveis de ambiente do usuário.<br/> |
| 0x40000000 | Anexar. Esse bit é opcional. Não defina os modificadores Append e Prefix.<br/>                                                                                            |
| 0x80000000 | Prefixo. Esse bit é opcional. Não defina os modificadores Append e Prefix.<br/>                                                                                            |



 

 

 




