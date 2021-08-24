---
description: ICE83 valida a tabela MsiAssembly.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e8014f8feee76e4d1910fb601e186bec928a0fd6d6d34469ce2c2b201b724d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580746"
---
# <a name="ice83"></a>ICE83

ICE83 valida a [tabela MsiAssembly](msiassembly-table.md). Essa ação personalizada de ICE posta um erro se o caminho de chave para um componente que contém um assembly Win32 é definido como o arquivo de manifesto. Explicitamente, o erro será postado se o valor inserido no campo KeyPath da [tabela de componentes](component-table.md) for igual ao valor inserido no \_ campo manifesto do arquivo da tabela MsiAssembly. Essa ação personalizada de ICE posta um erro se houver pelo menos um registro na tabela MsiAssembly e a [tabela InstallExecuteSequence](installexecutesequence-table.md) não contiver a [ação MsiPublishAssemblies](msipublishassemblies-action.md) e a [ação MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

## <a name="result"></a>Resultado

ICE83 posta os erros a seguir.



| Erro de ICE83                                                                                                   | Descrição                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O caminho da chave para o assembly do Win32 SxS (componente \_ = \[ 1 \] ) não deve ser seu arquivo de manifesto                       | ICE83 lança esse erro quando o campo KeyPath de um assembly Win32 é definido como seu arquivo de manifesto (Component. KeyPath = = MsiAssembly. File \_ manifest). \[1 \] é KeyPath na tabela de componentes                          |
| As ações MsiPublishAssemblies e MsiUnpublishAssemblies devem estar presentes na tabela InstallExecuteSequence. | ICE83 lança esse erro quando há pelo menos uma entrada na tabela MsiAssembly, mas a tabela InstallExecuteSequence não contém a ação MsiAssemblyPublish e a ação MsiAssemblyUnpublish. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



