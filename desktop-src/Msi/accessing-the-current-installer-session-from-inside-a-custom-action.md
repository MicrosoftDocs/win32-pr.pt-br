---
description: Nondeferred ações personalizadas que chamam scripts ou bibliotecas de vínculo dinâmico podem acessar uma instalação em execução para consultar ou modificar os atributos da sessão de instalação atual.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Acessando a sessão do instalador atual de dentro de uma ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a870247f70742d408c0f5d1d0e67f20cef65d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921536"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a>Acessando a sessão do instalador atual de dentro de uma ação personalizada

Nondeferred ações personalizadas que chamam [scripts](scripts.md) ou [bibliotecas de vínculo dinâmico](dynamic-link-libraries.md) podem acessar uma instalação em execução para consultar ou modificar os atributos da sessão de instalação atual. Somente um objeto de **sessão** pode existir para cada processo e os scripts de ação personalizada não devem tentar criar outra sessão.

As ações personalizadas só podem adicionar, modificar ou remover linhas, colunas ou tabelas temporárias de um banco de dados. As ações personalizadas não podem modificar dados persistentes em um banco de dados, como, por exemplo, aqueles que fazem parte dele armazenados no disco.

[Bibliotecas de vínculo dinâmico](dynamic-link-libraries.md)

Para acessar uma instalação em execução, ações personalizadas que chamam bibliotecas de vínculo dinâmico (DLL) são passadas para um identificador do tipo MSIHANDLE para a sessão atual como o único argumento para o ponto de entrada de DLL chamado na coluna de destino da [tabela CustomAction](customaction-table.md). Como o instalador fornece esse identificador, a ação personalizada não deve fechá-lo, por exemplo, para receber o identificador *hInstall* do instalador, a função de ação personalizada é declarada da seguinte maneira.


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Para acesso somente leitura ao banco de dados atual, obtenha o identificador de banco de dados chamando [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase). Para obter mais informações, consulte [obtendo um identificador de banco de dados](obtaining-a-database-handle.md).

[Scripts](scripts.md)

Ações personalizadas escritas em VBScript ou JScript podem acessar a sessão de instalação atual usando o [**objeto de sessão**](session-object.md). O instalador cria um objeto de **sessão** chamado "sessão" que faz referência à instalação atual. Para acesso somente leitura ao banco de dados atual, use a propriedade de [**banco de dados**](session-database.md) do objeto de **sessão** .

Como um script é executado a partir do contexto do objeto [**Session**](session-object.md) , nem sempre é necessário qualificar totalmente as propriedades e os métodos. No exemplo a seguir, ao usar o VBScript, a referência me pode substituir o objeto **Session** , por exemplo, as três linhas a seguir são equivalentes.


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[Arquivos executáveis](executable-files.md)

Você não pode acessar a sessão do instalador atual de ações personalizadas que chamam arquivos executáveis iniciados com uma linha de comando, por exemplo, [tipo de ação personalizada 2](custom-action-type-2.md) e [tipo de ação personalizada 18](custom-action-type-18.md).

[Ações personalizadas de execução adiada](deferred-execution-custom-actions.md)

Você não pode acessar a sessão do instalador atual ou todos os dados de propriedade de uma ação personalizada de execução adiada. Para obter mais informações, consulte [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando um banco de dados ou sessão de dentro de uma ação personalizada](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



