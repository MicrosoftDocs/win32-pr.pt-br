---
description: A tabela MsiServiceConfigFailureActions lista as operações a serem executadas depois que um serviço falha. As operações especificadas nesta tabela serão executadas na próxima vez em que o sistema for iniciado.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Tabela MsiServiceConfigFailureActions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae55d095e227611271de35d673289fc9eb5b174e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769313"
---
# <a name="msiserviceconfigfailureactions-table"></a>Tabela MsiServiceConfigFailureActions

A tabela MsiServiceConfigFailureActions lista as operações a serem executadas depois que um serviço falha. As operações especificadas nesta tabela serão executadas na próxima vez em que o sistema for iniciado.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Esta tabela está disponível a partir do Windows Installer 5,0.

A tabela MsiServiceConfigFailureActions tem as colunas a seguir.



| Coluna                         | Tipo                         | Chave | Nullable |
|--------------------------------|------------------------------|-----|----------|
| MsiServiceConfigFailureActions | [Identificador](identifier.md) | S   | N        |
| Nome                           | [Binário](formatted.md)   | N   | N        |
| Evento                          | [Inteiro](integer.md)       | N   | N        |
| ResetPeriod                    | [Inteiro](integer.md)       | N   | S        |
| RebootMessage                  | [Binário](formatted.md)   | N   | Y        |
| Comando                        | [Binário](formatted.md)   | N   | S        |
| Ações                        | [Text](text.md)             | N   | S        |
| DelayActions                   | [Text](text.md)             | N   | S        |
| Componente\_                    | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions
</dt> <dd>

Esta é a chave primária desta tabela que identifica uma ação de falha.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Esta coluna contém o nome de um serviço que faz parte deste pacote ou que já está instalado.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Circunstância
</dt> <dd>

Esta coluna especifica quando alterar a configuração do serviço. Os valores a seguir são campos de bits que podem ser combinados para representar várias operações. Qualquer outro valor de campo de bit é ignorado.



| Constante                                         | Descrição                                     |
|--------------------------------------------------|-------------------------------------------------|
| **msidbServiceConfigEventInstall** 1<br/>   | Alteração durante a instalação do componente.    |
| **msidbServiceConfigEventUninstall** 2<br/> | Alterar durante a desinstalação do componente.  |
| **msidbServiceConfigEventReinstall** 4<br/> | Alteração durante a reinstalação do componente. |



 

</dd> <dt>

<span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod
</dt> <dd>

O período de redefinição em segundos de contagem de falhas do serviço. O SCM ( [Gerenciador de controle de serviço](../services/service-control-manager.md) ) conta o número de vezes que cada serviço falhou desde que o sistema foi reiniciado pela última vez. A contagem será redefinida para zero se o serviço não falhar durante o período de redefinição. Quando o serviço falha durante o enésimo horário, o sistema executa a ação especificada no elemento \[ N-1 \] da matriz especificada no campo ações.

Deixe o campo ResetPeriod vazio para indicar que a contagem de falhas nunca deve ser redefinida.

</dd> <dt>

<span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage
</dt> <dd>

A mensagem enviada aos usuários antes de reiniciar o computador em resposta a uma ação **de \_ \_ reinicialização de ação SC** especificada na coluna ações. Você pode usar uma cadeia de caracteres vazia, "", para enviar a mensagem atual inalterada. Você pode usar \[ ~ \] a sintaxe do tipo de dados [formatado](formatted.md) para excluir a mensagem atual e não enviar nenhuma mensagem.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Linha
</dt> <dd>

A linha de comando executada pelo processo criado pela função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) em resposta a uma ação **de \_ \_ \_ comando de execução de ação SC** especificada na coluna ações. O novo processo é executado na mesma conta que o serviço e somente se o campo de ação **é \_ \_ \_ comando de execução de ação SC**. Você pode usar uma cadeia de caracteres vazia, "", para usar a linha de comando atual inalterada. Você pode usar a \[ ~ \] sintaxe do tipo de dados [formatado](formatted.md) para excluir a linha de comando atual e não executar nenhuma operação quando o serviço falhar.

</dd> <dt>

<span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Ações
</dt> <dd>

Esse campo contém uma matriz de valores inteiros que especificam as ações executadas pelo SCM se o serviço falhar. Separe os valores na matriz por \[ ~ \] . O valor inteiro no elemento enésima da matriz Especifica a ação executada quando o serviço falha durante o enésimo horário. Cada membro da matriz é um dos valores inteiros a seguir.



| Constante                                 | Descrição           |
|------------------------------------------|-----------------------|
| **Sc \_ AÇÃO \_ nenhum** 0<br/>         | Nenhuma ação.            |
| **Sc \_ AÇÃO \_ reinicializar** 2<br/>       | Reinicie o computador. |
| **Sc \_ AÇÃO \_ reiniciada** 1<br/>      | Reinicie o serviço.  |
| **Sc \_ \_ \_ Comando de execução de ação** 3<br/> | Execute um comando.        |



 

</dd> <dt>

<span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions
</dt> <dd>

Este campo contém uma matriz de valores inteiros que especificam o tempo em milissegundos a aguardar antes de executar a ação especificada na coluna ação. Separe os valores na matriz por \[ ~ \] . O número de elementos na matriz DelayActions deve ser igual ao número de elementos na matriz actions. O enésimo elemento da matriz DelayActions especifica o atraso de tempo para o enésimo elemento da matriz actions.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa para a coluna um da [tabela de componentes](component-table.md).

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

 

 
