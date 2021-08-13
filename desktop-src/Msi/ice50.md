---
description: ICE50 verifica se os ícones de atalho estão especificados para exibição correta e correspondem à extensão do arquivo de destino.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b9dd81c84c52738ee58c023ba5727cd6d5766bf7c40db97b6459483d7f53d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635147"
---
# <a name="ice50"></a>ICE50

ICE50 verifica se os ícones de atalho estão especificados para exibição correta e correspondem à extensão do arquivo de destino.

## <a name="result"></a>Result

ICE50 posta uma mensagem de erro se a extensão do ícone e dos arquivos de destino não coincidem. ICE50 posta um aviso se os ícones são armazenados em arquivos que não têm uma extensão .exe ou. ico.

## <a name="example"></a>Exemplo

ICE50 relata o seguinte erro para o exemplo mostrado.



| Erro ou aviso do ICE50                                                                                                              | Descrição                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A extensão do ícone ' Icon2. dat ' para o atalho ' Shortcut2 ' não corresponde à extensão do arquivo de chave para o componente ' Component2 '. | Se as extensões do ícone e o arquivo de destino não corresponderem, o atalho não terá o menu de contexto correto quando o componente for anunciado. Para corrigir esse erro, renomeie o ícone para corresponder à extensão do arquivo de destino.<br/> |
| A extensão do ícone ' Icon1.bat ' para o atalho ' Shortcut1 ' não é "exe" ou "ico". O ícone não será exibido corretamente.         | Nem todas as versões do Shell exibem corretamente os ícones armazenados em arquivos que não têm extensões de "exe" ou "ico". Para corrigir esse aviso, renomeie o ícone tem uma extensão de "exe" ou "ico".<br/>                                      |



 

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | FileName  |
|-------|-----------|
| Arquivo1 | File1.bat |
| Arquivo2 | File2.pl  |



 

[Tabela de recursos](feature-table.md) (parcial)



| Recurso  |
|----------|
| Feature1 |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente  | KeyPath |
|------------|---------|
| Component1 | Arquivo1   |
| Component2 | Arquivo2   |



 

[Tabela de ícones](icon-table.md)



| Name      | Dados            |
|-----------|-----------------|
| Icon1.bat | \[Binary Data\] |
| Icon2. dat | \[Binary Data\] |



 

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | Componente  | Destino   | Ícone\_    |
|-----------|------------|----------|-----------|
| Shortcut1 | Component1 | Feature1 | Icon1.bat |
| Shortcut2 | Component2 | Feature1 | Icon2. dat |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




