---
description: ICE69 verifica se todas as subcadeias de caracteres do formulário \[ $componentkey \] em uma cadeia de caracteres formatada não fazem referência cruzada de componentes.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171142"
---
# <a name="ice69"></a>ICE69

ICE69 verifica se todas as subcadeias de caracteres do formulário \[ $componentkey \] em uma cadeia de caracteres [formatada](formatted.md) não fazem referência cruzada de componentes. Uma referência entre componentes ocorre quando a \[ propriedade $componentkey \] de uma cadeia de caracteres formatada refere-se a um componente que não é o componente armazenado na \_ coluna componente de suas tabelas.

Problemas com referências entre componentes surgem da maneira como as cadeias de caracteres [formatadas](formatted.md) são avaliadas. Se o componente referenciado com \[ a \] Propriedade $componentkey já estiver instalado e não estiver sendo alterado durante a instalação atual (por exemplo, sendo reinstalado, movido para a origem e assim por diante), a expressão \[ $componentkey \] será avaliada como NULL, porque o estado de ação do componente em \[ $componentkey \] é nulo. Problemas semelhantes podem ocorrer durante as operações de atualização e reparo.

## <a name="result"></a>Resultado

ICE69 retornará um erro se uma \[ \] subcadeia de caracteres $componentkey dentro de uma cadeia de caracteres [formatada](formatted.md) cruzar referências a um componente em outro recurso. ICE69 retornará um aviso se uma \[ \] subcadeia de caracteres $componentkey dentro de uma cadeia de caracteres formatada cruzar referências a um componente no mesmo recurso. (A tabela [FeatureComponents](featurecomponents-table.md) é usada para determinar esse mapeamento. Ele deve mapear para o mesmo recurso para o aviso. A referência a componentes em recursos pai ou referência a componentes em recursos filho é considerada um erro.)

ICE69 relatará um erro se a \[ \# \] subcadeia de caracteres FileKey dentro de uma cadeia de caracteres [formatada](formatted.md) fizer referência a um arquivo que não está especificado na tabela de [arquivos](file-table.md) como pertencente ao mesmo componente.

## <a name="example"></a>Exemplo

ICE69 relata o seguinte para os exemplos mostrados.

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

Para corrigir esse erro, não faça referência cruzada de componentes. Altere o \[ $componentkey \] para corresponder ao componente do atalho.

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | Componente\_ | Argumento     |
|-----------|-------------|--------------|
| Teste      | QuickTest   | -v \[ $Test\] |
| Shortcut2 | QuickTest   | \[$Test 2\]   |



 

As tabelas de [verbo](verb-table.md) e de [extensão](extension-table.md) são casos especiais em que a tabela de verbos faz referência a uma extensão que pertence a um componente. No entanto, uma extensão pode pertencer a vários componentes porque a chave primária para a tabela de extensão é composta pelas colunas de extensão e componente \_ . Logicamente, você pode ter a seguinte situação.

[Tabela de verbos](verb-table.md) (parcial)



| Extensão | Verbo\_ | Argumento                |
|-----------|--------|-------------------------|
| TST       | Abrir   | -v \[ $comp 1 \] \[ $comp 2\] |



 

[Tabela de extensão](extension-table.md) (parcial)



| Extensão | Componente\_ |
|-----------|-------------|
| TST       | comp1       |
| TST       | COMP2       |



 

[Tabela FeatureComponents](featurecomponents-table.md)



| Recurso\_ | Componente\_ |
|-----------|-------------|
| Feature1  | QuickTest   |
| Feature1  | Teste        |
| Feature2  | Test2       |



 

Nesse caso, você deve garantir que pelo menos uma das propriedades de \[ $componentkey \] seja avaliada como um valor não nulo. No entanto, cada \[ \] Propriedade $componentkey na coluna Argument da tabela Verb ( \[ $comp 1 \] e \[ $comp 2 \] no exemplo acima) deve fazer referência a um possível componente incluído com a extensão associada ao verbo. Uma referência como \[ $comp 3 \] resultaria em um aviso de ICE69.

A [tabela AppID](appid-table.md) tem uma situação semelhante à tabela de verbos. Ele usa a [tabela de classes](class-table.md) para sua referência de componente. Nesse caso, a tabela AppId é validada da mesma maneira que a validação de Verb-Extension (agora, a classe AppId).

A coluna de argumento da tabela de classes é validada como o [atalho](shortcut-table.md), o [registro](registry-table.md)e as tabelas semelhantes.

## <a name="table-used-during-execution-only-if-found"></a>Tabela usada durante a execução (somente se encontrada)

[IniFile](inifile-table.md)

[RemoveIniFile](removeinifile-table.md)

[Registro](registry-table.md)

[RemoveRegistry](removeregistry-table.md)

[ServiceControl](servicecontrol-table.md)

[Instalar o](serviceinstall-table.md)

[Atalho](shortcut-table.md)

[Verbo](verb-table.md)

[Extensão](extension-table.md)

[Classe](class-table.md)

[AppId](appid-table.md)

[Ambiente](environment-table.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



