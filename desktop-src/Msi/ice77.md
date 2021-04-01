---
description: ICE77 verifica se as ações personalizadas com o conjunto de bits msidbCustomActionTypeInScript são sequenciadas após a ação InstallInitialize e antes da ação InstallFinalize.
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e072692b76cfd63bf62c5fd23f612a445e5fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090782"
---
# <a name="ice77"></a>ICE77

ICE77 verifica se as ações personalizadas com o conjunto de bits **msidbCustomActionTypeInScript** são sequenciadas após a [ação InstallInitialize](installinitialize-action.md) e antes da [ação InstallFinalize](installfinalize-action.md). ICE77 verifica a sequência na [tabela InstallExecuteSequence](installexecutesequence-table.md) e na [tabela AdminExecuteSequence](adminexecutesequence-table.md).

## <a name="result"></a>Resultado

ICE77 posta um erro se uma ação personalizada em script for sequenciada antes da ação InstallInitialize ou após a ação InstallFinalize.

ICE77 lançará um erro se a ação InstallInitialize ou a ação InstallFinalize estiver ausente.

## <a name="example"></a>Exemplo

ICE77 relata os seguintes erros para o exemplo:

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

[Tabela CustomAction](customaction-table.md) (parcial)



| Ação              | Tipo |
|---------------------|------|
| \_INSCRIPTINSTALL CA | 1025 |
| \_INSCRIPTADMIN CA   | 1026 |



 

[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Ação              | Sequência |
|---------------------|----------|
| \_INSCRIPTINSTALL CA | 2000     |
| InstallInitialize   | 1500     |



 

[Tabela AdminExecuteSequence](adminexecutesequence-table.md) (parcial)



| Ação            | Sequência |
|-------------------|----------|
| \_INSCRIPTADMIN CA | 1.400     |
| InstallInitialize | 1500     |
| InstallFinalize   | 6600     |



 

Para corrigir os erros, sequenciar as ações personalizadas em script após a ação InstallInitialize e antes da ação InstallFinalize. As ações InstallInitialize e InstallFinalize devem estar presentes na tabela InstallExecuteSequence e na tabela AdminExecuteSequence.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



