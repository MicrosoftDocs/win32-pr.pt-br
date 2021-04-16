---
description: ICE59 verifica se os atalhos anunciados pertencem aos componentes instalados pelo recurso de destino do atalho.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752455"
---
# <a name="ice59"></a>ICE59

ICE59 verifica se os atalhos anunciados pertencem aos componentes instalados pelo recurso de destino do atalho.

Os erros relatados por ICE59 geralmente levam ao seguinte comportamento:

1.  O atalho anunciado iniciará o Windows Installer para instalar o recurso listado na coluna de destino.
2.  Mas como a [tabela FeatureComponents](featurecomponents-table.md) não mapeia o recurso de destino para o componente que contém o atalho, o keyfile do componente (que é ativado pelo atalho) não é instalado.
3.  Portanto, o atalho é quebrado e não fará nada.

## <a name="result"></a>Resultado

ICE59 posta um erro se um atalho anunciado não pertencer aos componentes instalados pelo recurso de destino do atalho.

## <a name="example"></a>Exemplo

ICE59 relata o seguinte erro para o exemplo mostrado:

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

Nesse caso, ShortcutB anuncia o recurso e, quando ativado, inicia o arquivo de chave de ComponentB. Ainda assim, o ComponentB nunca é instalado pelo Recursoa, então mesmo após a fase de instalação sob demanda ser concluída, o destino do atalho não existe.

Para corrigir esse erro, adicione uma linha à [tabela FeatureComponents](featurecomponents-table.md) que associa o recurso e o ComponentB.

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | Destino   | Componente\_ |
|-----------|----------|-------------|
| ShortcutB | Recurso | ComponentB  |



 

[Tabela FeatureComponents](featurecomponents-table.md)



| Recurso\_ | Componente\_ |
|-----------|-------------|
| Recurso  | Componente  |



 

[Tabela de recursos](feature-table.md) (parcial)



| Recurso  | Nível |
|----------|-------|
| Recurso | 10    |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente  | KeyPath |
|------------|---------|
| Componente | FileA   |
| ComponentB | FileB   |



 

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Componente\_ | Sequência |
|-------|-------------|----------|
| FileA | Componente  | 1        |
| FileB | ComponentB  | 2        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



