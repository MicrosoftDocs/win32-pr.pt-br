---
description: A tabela MsiServiceConfigFailureActions lista as operações a serem executados depois que um serviço falha. As operações especificadas nesta tabela são executados na próxima vez que o sistema for iniciado.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Tabela MsiServiceConfigFailureActions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907c0feb2e331c1e19ff4292d11cc58b65340a7543d9af5d0a1ccf23d2e80a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944413"
---
# <a name="msiserviceconfigfailureactions-table"></a>Tabela MsiServiceConfigFailureActions

A tabela MsiServiceConfigFailureActions lista as operações a serem executados depois que um serviço falha. As operações especificadas nesta tabela são executados na próxima vez que o sistema for iniciado.

**[Windows Instalador 4.5 ou anterior:](not-supported-in-windows-installer-4-5.md)** Sem suporte. Esta tabela está disponível a partir do Windows Instalador 5.0.

A tabela MsiServiceConfigFailureActions tem as colunas a seguir.



| Coluna                         | Tipo                         | Chave | Nullable |
|--------------------------------|------------------------------|-----|----------|
| MsiServiceConfigFailureActions | [Identificador](identifier.md) | Y   | N        |
| Nome                           | [Formatado](formatted.md)   | N   | N        |
| Evento                          | [Inteiro](integer.md)       | N   | N        |
| ResetPeriod                    | [Inteiro](integer.md)       | N   | Y        |
| RebootMessage                  | [Formatado](formatted.md)   | N   | Y        |
| Comando                        | [Formatado](formatted.md)   | N   | Y        |
| Ações                        | [Text](text.md)             | N   | Y        |
| DelayActions                   | [Text](text.md)             | N   | Y        |
| Componente\_                    | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions
</dt> <dd>

Essa é a chave primária desta tabela que identifica uma ação de falha.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Esta coluna contém o nome de um serviço que faz parte desse pacote ou que já está instalado.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Evento
</dt> <dd>

Essa coluna especifica quando alterar a configuração do serviço. Os valores a seguir são campos de bits que podem ser combinados para representar várias operações. Quaisquer outros valores de campo de bits são ignorados.



| Constante                                         | Descrição                                     |
|--------------------------------------------------|-------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Alteração durante a instalação do componente.    |
| **msidbServiceConfigEventUninstall** 2<br/> | Alteração durante a desinstalação do componente.  |
| **msidbServiceConfigEventReinstall** 4<br/> | Alteração durante a re-instalação do componente. |



 

</dd> <dt>

<span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod
</dt> <dd>

O período de redefinição em segundos da contagem de falhas do serviço. O [SCM (Service Control Manager)](../services/service-control-manager.md) conta o número de vezes que cada serviço falhou desde que o sistema foi reiniciado pela última vez. A contagem será redefinida como zero se o serviço não falhar durante o período de redefinição. Quando o serviço falha pela Nª vez, o sistema executa a ação especificada no elemento N-1 da matriz especificada no \[ \] campo Ações.

Deixe o campo ResetPeriod vazio para indicar que a contagem de falhas nunca deve ser redefinida.

</dd> <dt>

<span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage
</dt> <dd>

A mensagem enviada aos usuários antes de reiniciar o computador em resposta a uma ação **SC \_ ACTION \_ REBOOT** especificada na coluna Ações. Você pode usar uma cadeia de caracteres vazia, "", para enviar a mensagem atual inalterada. Você pode usar \[ ~ \] a sintaxe do tipo [de dados](formatted.md) Formatado para excluir a mensagem atual e não enviar nenhuma mensagem.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Comando
</dt> <dd>

A linha de comando é executado pelo processo criado pela função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) em resposta a uma ação **SC ACTION RUN \_ \_ \_ COMMAND** especificada na coluna Ações. O novo processo é executado na mesma conta que o serviço e somente se o campo Ação for **SC \_ ACTION RUN \_ \_ COMMAND**. Você pode usar uma cadeia de caracteres vazia, "", para usar a linha de comando atual inalterada. Você pode usar a sintaxe do tipo de dados Formatado para excluir a linha de comando atual e não \[ ~ \] executar nenhuma operação quando o serviço falhar. [](formatted.md)

</dd> <dt>

<span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Ações
</dt> <dd>

Esse campo contém uma matriz de valores inteiros que especificam as ações tomadas pelo SCM se o serviço falhar. Separe os valores na matriz por \[ ~ \] . O valor inteiro no Nº elemento da matriz especifica a ação executada quando o serviço falha pela Nª vez. Cada membro da matriz é um dos seguintes valores inteiros.



| Constante                                 | Descrição           |
|------------------------------------------|-----------------------|
| **SC \_ ACTION \_ NONE** 0<br/>         | Nenhuma ação.            |
| **SC \_ ACTION \_ REBOOT** 2<br/>       | Reinicie o computador. |
| **SC \_ ACTION \_ RESTART** 1<br/>      | Reinicie o serviço.  |
| **SC \_ COMANDO \_ ACTION \_ RUN** 3<br/> | Execute um comando .        |



 

</dd> <dt>

<span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions
</dt> <dd>

Esse campo contém uma matriz de valores inteiros que especificam o tempo em milissegundos para aguardar antes de executar a ação especificada na coluna Ação. Separe os valores na matriz por \[ ~ \] . O número de elementos na matriz DelayActions deve ser igual ao número de elementos na matriz Actions. O Nº elemento da matriz DelayActions especifica o atraso de tempo para o nº elemento da matriz Actions.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa para a coluna um da [Tabela de Componentes](component-table.md).

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE102](ice-102.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 
