---
description: ICE69 verifica se todas as substrings do formulário $componentkey em uma cadeia de caracteres formatada não fazem referência cruzada a \[ \] componentes.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183a62989ff39387639af1a9e1feeeddc3e0567f28915ca3857ba6dd5f58f68c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043936"
---
# <a name="ice69"></a>ICE69

ICE69 verifica se todas as substrings do formulário $componentkey em uma cadeia de caracteres formatada não fazem referência cruzada a \[ \] componentes. [](formatted.md) Uma referência entre componentes ocorre quando a $componentkey de uma cadeia de caracteres formatada refere-se a um componente diferente do componente armazenado na coluna \[ \] Componente de suas \_ tabelas.

Problemas com referência entre componentes surgem da maneira como cadeias de caracteres [formatadas](formatted.md) são avaliadas. Se o componente referenciado com a propriedade $componentkey já estiver instalado e não estiver sendo alterado durante a instalação atual \[ (por exemplo, sendo reinstalado, movido para a origem e assim por diante), a expressão $componentkey será avaliada como nula, porque o estado de ação do componente no $componentkey \] \[ é \] \[ \] nulo. Problemas semelhantes podem ocorrer durante operações de atualização e reparo.

## <a name="result"></a>Resultado

ICE69 retornará um erro se $componentkey substring em uma cadeia de caracteres formatada faz referência \[ cruzada a um componente em outro \] recurso. [](formatted.md) ICE69 retorna um aviso se $componentkey substring em uma cadeia de caracteres formatada faz referência cruzada a um componente \[ \] no mesmo recurso. (A [tabela FeatureComponents](featurecomponents-table.md) é usada para determinar esse mapeamento. Ele deve mapear para o mesmo recurso para o aviso. A referência de componentes em recursos pai ou a referência de componentes em recursos filho é considerada um erro.)

ICE69 relata um erro se \[ \# \] a substring [](formatted.md) [](file-table.md) FileKey em uma cadeia de caracteres formatada faz referência a um arquivo que não está especificado na tabela Arquivo como pertencente ao mesmo componente.

## <a name="example"></a>Exemplo

ICE69 relata o seguinte para os exemplos mostrados.

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

Para corrigir esse erro, não faça referência cruzada a componentes. Altere \[ $componentkey \] para corresponder ao componente do atalho.

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | Componente\_ | Argumento     |
|-----------|-------------|--------------|
| Teste      | Quicktest   | -v \[ $Test\] |
| Atalho2 | Quicktest   | \[$Test 2\]   |



 

As [tabelas](verb-table.md) Verbo [e](extension-table.md) Extensão são casos especiais em que a tabela Verb faz referência a uma extensão que pertence a um componente. No entanto, uma Extensão pode pertencer a vários componentes porque a chave primária da tabela de extensão é feita das colunas Extensão \_ e Componente. Logicamente, você pode ter a seguinte situação.

[Tabela de verbos](verb-table.md) (parcial)



| Extensão | Verbo\_ | Argumento                |
|-----------|--------|-------------------------|
| Tst       | Abrir   | -v \[ $comp 1 \] \[ $comp 2\] |



 

[Tabela de extensão](extension-table.md) (parcial)



| Extensão | Componente\_ |
|-----------|-------------|
| Tst       | comp1       |
| Tst       | comp2       |



 

[Tabela FeatureComponents](featurecomponents-table.md)



| Recurso\_ | Componente\_ |
|-----------|-------------|
| Feature1  | Quicktest   |
| Feature1  | Teste        |
| Feature2  | Test2       |



 

Nesse caso, você deve garantir que pelo menos uma das propriedades $componentkey seja avaliada como \[ \] um valor não nulo. No entanto, cada $componentkey na coluna Argument da tabela \[ \] Verb ( $comp 1 e \[ \] \[ $comp 2 \] no exemplo acima) deve referenciar um possível componente incluído com a extensão associada ao verbo. Uma referência como \[ $comp 3 \] resultaria em um aviso de ICE69.

A [tabela AppId](appid-table.md) tem uma situação semelhante à tabela Verb. Ele usa a [tabela Classe para](class-table.md) sua referência de componente. Nesse caso, a tabela AppId é validada da mesma maneira que a validação de Verb-Extension (agora AppId-Class).

A coluna Argumento da tabela Class é validada como [Atalho,](shortcut-table.md) [Registro](registry-table.md)e tabelas semelhantes.

## <a name="table-used-during-execution-only-if-found"></a>Tabela usada durante a execução (somente se encontrada)

[IniFile](inifile-table.md)

[RemoveIniFile](removeinifile-table.md)

[Registro](registry-table.md)

[RemoveRegistry](removeregistry-table.md)

[ServiceControl](servicecontrol-table.md)

[ServiceInstall](serviceinstall-table.md)

[Atalho](shortcut-table.md)

[Verbo](verb-table.md)

[Extensão](extension-table.md)

[Classe](class-table.md)

[Appid](appid-table.md)

[Ambiente](environment-table.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



