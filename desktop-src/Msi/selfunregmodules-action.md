---
description: A ação SelfUnregModules cancela o registro de todos os módulos listados na tabela SelfReg que estão agendados para serem desinstalados. O instalador não registra automaticamente .EXE arquivos.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: Ação SelfUnregModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ba95a745716d512a72e9541064f56bdc663e2e6c9658a9c35744449217952f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040326"
---
# <a name="selfunregmodules-action"></a>Ação SelfUnregModules

A ação SelfUnregModules cancela o registro de todos os módulos listados na [tabela selfreg](selfreg-table.md) que estão agendados para serem desinstalados. O instalador não registra automaticamente .EXE arquivos.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação [InstallValidate](installvalidate-action.md) deve aparecer antes da ação SelfUnregModules na sequência. Se uma ação [SelfRegModules](selfregmodules-action.md) for usada, ela deverá aparecer após a ação SelfUnregModules na sequência. Se uma [ação removes](removefiles-action.md) for usada, ela deverá aparecer após a ação SelfUnregModules na sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                             |
|-------|--------------------------------------------------------|
| \[1\] | Identificador do arquivo de módulo não registrado.                |
| \[2\] | Identificador da pasta que contém o arquivo de módulo não registrado. |



 

## <a name="remarks"></a>Comentários

A ação SelfUnregModules tenta chamar a função [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) do módulo cujo registro deve ser cancelado. Essa ação é executada com privilégios elevados quando a instalação está sendo executada com privilégios elevados, como durante uma instalação por máquina. Durante uma instalação por usuário, o instalador executa essa ação com privilégios de usuário.

Observe que você não pode especificar a ordem na qual o instalador cancela o registro de DLLs de registro automático usando a ação SelfUnRegModules.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificando a ordem de auto-registro](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
