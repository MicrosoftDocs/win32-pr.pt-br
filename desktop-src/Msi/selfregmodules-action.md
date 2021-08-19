---
description: A ação SelfRegModules processa todos os módulos listados na tabela SelfReg e registra todos os módulos instalados no sistema. O instalador não registra arquivos EXE por conta própria.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: Ação SelfRegModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf137dc63baa72a3d5b93370e40911af93691eaa911c4081990656c84091870
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630036"
---
# <a name="selfregmodules-action"></a>Ação SelfRegModules

A ação SelfRegModules processa todos os módulos listados na tabela [SelfReg](selfreg-table.md) e registra todos os módulos instalados no sistema. O instalador não registra arquivos EXE por conta própria.

## <a name="sequence-restrictions"></a>Restrições de sequência

A [ação InstallValidate](installvalidate-action.md) deve ser chamada antes de chamar a ação SelfRegModules. Se uma [ação InstallFiles](installfiles-action.md) for usada, ela deverá aparecer antes da ação SelfRegModules na sequência. Como a ação SelfRegModules altera o sistema, SelfRegModules deve vir após a [ação InstallInitialize](installinitialize-action.md).

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação                           |
|-------|------------------------------------------------------|
| \[1\] | Identificador do arquivo de módulo registrado.                |
| \[2\] | Identificador da pasta que mantém o arquivo de módulo registrado. |



 

## <a name="remarks"></a>Comentários

A ação SelfRegModules tenta chamar a [função DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) do módulo agendado para ser registrado. Essa ação é executado com privilégios elevados quando a instalação está sendo executado com privilégios elevados, como durante uma instalação por computador. Durante uma instalação por usuário, o instalador executa essa ação com privilégios de usuário.

Observe que você não pode especificar a ordem na qual o instalador registra DLLs de auto-registro usando a [ação SelfUnRegModules](selfunregmodules-action.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificando a ordem de auto-registro](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
