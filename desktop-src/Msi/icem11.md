---
description: ICEM11 verifica se um módulo de mesclagem configurável lista a Tabela ModuleConfiguration e a tabela ModuleSubstitution na tabela ModuleIgnoreTable do módulo.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 157248d62f43a0b1a791220e2aeb917ba8273d31b93de69078f9876cddbd2748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894426"
---
# <a name="icem11"></a>ICEM11

ICEM11 verifica se um módulo de mesclagem configurável lista a [Tabela ModuleConfiguration](moduleconfiguration-table.md) e a [tabela ModuleSubstitution](modulesubstitution-table.md) na [tabela ModuleIgnoreTable](moduleignoretable-table.md) do módulo. Isso garante que as ferramentas de mesclagem que não reconheçam módulos de mesclagem configuráveis (menos que a versão 2,0) não copiem essas tabelas no banco de dados de destino.

esse ICEM está disponível no arquivo Mergemod. cub fornecido no SDK do Windows Installer 2,0 e posterior. para obter detalhes, consulte [SDK do Windows components for Windows Installer developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Resultado

ICEM11 lançará um erro se o módulo contiver uma tabela ModuleConfiguration ou ModuleSubstitution não listada na tabela ModuleIgnoreTable.

## <a name="example"></a>Exemplo

ICEM11 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas abaixo.

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

[ModuleConfiguration](moduleconfiguration-table.md) (parcial)



| Nome     | Formatar | Tipo   | ContextData | DefaultValue |
|----------|--------|--------|-------------|--------------|
| IconKey1 | 1      | Binário | ícone        | DefaultIcon  |



 

[ModuleSubstitution](modulesubstitution-table.md)



| Tabela   | Linha              | Coluna | Valor        |
|---------|------------------|--------|--------------|
| Control | Dialog1; Control1 | Texto   | \[IconKey1\] |



 

[ModuleIgnoreTable](moduleignoretable-table.md)



| Tabela               |
|---------------------|
| ModuleConfiguration |



 

Para corrigir esse erro, inclua as tabelas ModuleSubstitution e ModuleConfiguration na tabela ModuleIgnoreTable.

## <a name="table-used-during-execution"></a>Tabela usada durante a execução

[ModuleSubstitution](modulesubstitution-table.md)

[ModuleConfiguration](moduleconfiguration-table.md)

[ModuleIgnoreTable](moduleignoretable-table.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



