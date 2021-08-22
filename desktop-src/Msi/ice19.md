---
description: O ICE19 valida que os componentes anunciados fazem referência a um arquivo na coluna KeyPath da tabela de componentes e que um atalho anunciado faz referência a um diretório nesta coluna.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1a706999744762a930a800326cb8d38487f19c1c4ea3e01b6b1f8aeae4ca2dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529106"
---
# <a name="ice19"></a>ICE19

O ICE19 valida que os componentes anunciados fazem referência a um arquivo na coluna KeyPath da [tabela de componentes](component-table.md) e que um atalho anunciado faz referência a um diretório nesta coluna.

ICE19 valida que os componentes ou atalhos anunciados têm um ComponentID. Os componentes na [tabela PublishComponent](publishcomponent-table.md), que não são anunciados em outra tabela, só são verificados para ver se eles têm um ComponentID.

## <a name="result"></a>Resultado

ICE19 posta uma mensagem de erro se a coluna KeyPath da tabela Component não faz referência a um arquivo no caso de um componente anunciado ou um diretório no caso de um atalho anunciado. ICE19 posta uma mensagem de erro se algum componente ou atalho anunciado não tiver um ComponentID.

## <a name="example"></a>Exemplo

ICE19 posta as seguintes mensagens de erro para o exemplo mostrado:

-   A extensão FLP faz referência ao componente comp1 que não tem um ComponentID especificado na [tabela de componentes](component-table.md).
-   A extensão exe faz referência ao componente Comp4 que faz referência a um diretório como seu caminho KeyPath. O caminho keyé nulo na tabela de componentes.
-   O atalho Shortcut2 faz referência ao componente Comp3 que faz referência a uma entrada do registro como o caminho da chave. O valor da coluna atributos na tabela de componentes é 4.

[Tabela de componentes](component-table.md) (parcial)



| Componente | ComponentId                            | Atributos | KeyPath |
|-----------|----------------------------------------|------------|---------|
| Comp1     | Nulo                                   | 0          | Arquivo1   |
| Comp2     | {00000002-0003-0000-0000-624474736554} | 0          | Arquivo2   |
| Comp3     | {00000003-0003-0000-0000-624474736554} | 4          | Reg3    |
| Comp4     | {00000004-0003-0000-0000-624474736554} | 0          | Nulo    |



 

[Tabela de extensão](extension-table.md) (parcial)



| Extensão | Componente\_ |
|-----------|-------------|
| FLP       | Comp1       |
| TST       | Comp2       |
| exe       | Comp4       |



 

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | Componente\_ | Recurso\_      |
|-----------|-------------|----------------|
| Shortcut1 | Comp4       | ProductFeature |
| Shortcut2 | Comp3       | ProductFeature |



 

[Tabela de recursos](feature-table.md) (parcial)



| Recurso        |
|----------------|
| ProductFeature |



 

> [!Note]  
> Se a extensão FLP e o exe referenciarem o mesmo componente, o EXE ou o servidor COM que os abre deve ser o mesmo. Esse EXE é normalmente o caminho Keypara o componente. Para o OFFICE, as extensões doc e XLS não podem referenciar o mesmo componente porque o mesmo EXE não abre ambas as extensões. Você precisa winword.exe para abrir as extensões de documento e precisa excel.exe abrir as extensões xls.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



