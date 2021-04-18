---
description: A ação SelfRegModules processa todos os módulos listados na tabela SelfReg e registra todos os módulos instalados com o sistema. O instalador não registra automaticamente arquivos EXE.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: Ação SelfRegModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75895b1886fad51f36113ce6e677ba6a534ab0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753258"
---
# <a name="selfregmodules-action"></a>Ação SelfRegModules

A ação SelfRegModules processa todos os módulos listados na tabela [selfreg](selfreg-table.md) e registra todos os módulos instalados com o sistema. O instalador não registra automaticamente arquivos EXE.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação [InstallValidate](installvalidate-action.md) deve ser chamada antes de chamar a ação SelfRegModules. Se uma ação [InstallFiles](installfiles-action.md) for usada, ela deverá aparecer antes da ação SelfRegModules na sequência. Como a ação SelfRegModules altera o sistema, SelfRegModules deve vir após a [ação InstallInitialize](installinitialize-action.md).

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                           |
|-------|------------------------------------------------------|
| \[1\] | Identificador do arquivo de módulo registrado.                |
| \[2\] | Identificador da pasta que contém o arquivo de módulo registrado. |



 

## <a name="remarks"></a>Comentários

A ação SelfRegModules tenta chamar a função [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) do módulo agendado para ser registrado. Essa ação é executada com privilégios elevados quando a instalação está sendo executada com privilégios elevados, como durante uma instalação por máquina. Durante uma instalação por usuário, o instalador executa essa ação com privilégios de usuário.

Observe que você não pode especificar a ordem na qual o instalador registra DLLs de registro automático usando a [ação SelfUnRegModules](selfunregmodules-action.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificando a ordem de auto-registro](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
