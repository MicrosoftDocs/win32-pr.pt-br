---
description: O ICE17 verifica as situações mostradas no exemplo no final deste tópico.
ms.assetid: a1d9a6e9-4d21-4544-a813-dc82e11f5a26
title: ICE17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c296273e1de5ae633b2708c92cf0376018e6d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828980"
---
# <a name="ice17"></a>ICE17

O ICE17 verifica as situações mostradas no exemplo no final deste tópico.

## <a name="result"></a>Resultado

ICE17 exibe uma mensagem de erro ou de aviso para cada uma das situações no exemplo. Exemplos dessas mensagens são mostrados na tabela a seguir.



| Erro ou aviso do ICE17                                                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Botão de pressão: o Button1 da caixa de diálogo: MyDialog não tem um evento definido na tabela ControlEvent,. Erro <br/>                                                                                                                | Há um [controle de pressão](pushbutton-control.md) que não está listado na [tabela ControlEvent,](controlevent-table.md). Se ICE17 retornar esse erro em um botão de pressão para o qual o atributo **habilitar controle** ou o atributo de **controle visível** não esteja definido na coluna atributos da [tabela de controle](control-table.md), verifique se o controle também tem uma entrada na [tabela ControlCondition](controlcondition-table.md). O controle pode ser habilitado inesperadamente, ou visível, se o valor na coluna condição mudar para verdadeiro, habilitar ou mostrar.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| Bitmap: Bitmap1 de controle: Bitmap1 da caixa de diálogo: MyDialog não está na tabela binária. Erro <br/>                                                                                                                              | Há um [controle de bitmap](bitmap-control.md) ou [controle de ícone](icon-control.md), mas o bitmap ou ícone correspondente não está listado na [tabela binária](binary-table.md). Adicione o bitmap ou o ícone à tabela binária.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Botão de opção: RadioButton1 de Control: RadioButton1 da caixa de diálogo: MyDialog não está na tabela RadioButton. Aviso <br/>                                                                                                   | Há um [controle de botão de opção](radiobuttongroup-control.md) com valores na coluna Propriedade e na coluna atributo da tabela de [controle](control-table.md); o bit [indireto](indirect-control-attribute.md) não está definido na coluna atributos. ICE17 posta um aviso porque o instalador usa o valor da propriedade como uma chave estrangeira na tabela RadioButton, mas o valor está ausente da chave primária dessa tabela. Se o bit [indireto](indirect-control-attribute.md) estiver definido, a propriedade listada para o controle não será usada como a propriedade; em vez disso, ele é usado como o nome da propriedade que é realmente usada.<br/> Esse aviso poderá ser ignorado se o controle for criado em tempo de execução. Por exemplo, o [controle ListBox](listbox-control.md) para na [caixa de diálogo FilesInUse](filesinuse-dialog.md) é criado somente em tempo de execução se houver arquivos em uso durante a instalação.<br/> |
| ListBox: ListBox1 de Control: ListBox1 da caixa de diálogo: MyDialog não está na tabela ListBox. Aviso <br/>                                                                                                                        | Há um [controle ListBox](listbox-control.md) com um valor na coluna Property da [tabela de controle](control-table.md) e para o qual o bit [indireto](indirect-control-attribute.md) não está definido na coluna Attributes. ICE17 posta um aviso porque o instalador usa o valor da propriedade como uma chave estrangeira na [tabela ListBox](listbox-table.md), mas o valor está ausente da chave primária dessa tabela. Se o bit [indireto](indirect-control-attribute.md) estiver definido, o controle alterará o valor de uma propriedade que tem um nome que é o valor da propriedade associada a esse controle.<br/> Esse aviso poderá ser ignorado se o controle for criado em tempo de execução. Por exemplo, o [controle ListBox](listbox-control.md) para na [caixa de diálogo FilesInUse](filesinuse-dialog.md) é criado somente em tempo de execução se houver arquivos em uso durante a instalação.<br/>                                |
| ComboBox: ComboBox1 de Control: ComboBox1 da caixa de diálogo: ByDialog não está no aviso da tabela ComboBox <br/>                                                                                                                     | Há um [controle ComboBox](combobox-control.md) com um valor na coluna Property da [tabela de controle](control-table.md) e para o qual o bit [indireto](indirect-control-attribute.md) não está definido na coluna Attributes. ICE17 posta um aviso porque o instalador usa o valor da propriedade como uma chave estrangeira na [tabela ComboBox](combobox-table.md), mas o valor está ausente da chave primária dessa tabela. Se o bit [indireto](indirect-control-attribute.md) estiver definido, o controle alterará o valor de uma propriedade que tem um nome que é o valor da propriedade associada a esse controle.<br/> Esse aviso poderá ser ignorado se o controle for criado em tempo de execução. Por exemplo, o [controle ListBox](listbox-control.md) para na [caixa de diálogo FilesInUse](filesinuse-dialog.md) é criado somente em tempo de execução se houver arquivos em uso durante a instalação.<br/>                            |
| ListView: ListView1 de controle: ListView1 da caixa de diálogo: MyDialog não está na tabela ListView. Aviso <br/>                                                                                                                    | Há um [controle ListView](listview-control.md) com um valor na coluna Property da [tabela de controle](control-table.md) e para o qual o bit [indireto](indirect-control-attribute.md) não está definido na coluna Attributes. ICE17 posta um aviso porque o instalador usa o valor da propriedade como uma chave estrangeira na [tabela ListView](listview-table.md), mas o valor está ausente da chave primária dessa tabela. Se o bit [indireto](indirect-control-attribute.md) estiver definido, o controle alterará o valor de uma propriedade que tem um nome que é o valor da propriedade associada a esse controle.<br/> Esse aviso poderá ser ignorado se o controle for criado em tempo de execução. Por exemplo, o [controle ListBox](listbox-control.md) para na [caixa de diálogo FilesInUse](filesinuse-dialog.md) é criado somente em tempo de execução se houver arquivos em uso durante a instalação.<br/>                            |
| Bitmap: ' Bitmap2 ' para controle: ' Button2 ' da caixa de diálogo: ' MyDialog ' não encontrado no erro de tabela binária <br/>                                                                                                                         | Há um controle de [pressão](pushbutton-control.md) ou [controle de caixa de seleção](checkbox-control.md) para o qual a coluna de texto da [tabela de controle](control-table.md) não contém uma chave estrangeira no registro da [tabela binária](binary-table.md) que contém o bitmap ou ícone.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Bitmap: ' Bitmap3 ' para controle: ' RadioButton2 ' da caixa de diálogo: ' MyDialog ' não encontrado na tabela binary ou<br/> Ícone: ' icon1 ' para o controle: ' RadioButton3 ' da caixa de diálogo: ' MyDialog ' não encontrado na tabela binária<br/> Erro <br/> | Há um [controle de botão de opção](radiobuttongroup-control.md) para o qual a coluna de texto da [tabela RadioButton](radiobutton-table.md) não contém uma chave estrangeira no registro da [tabela binária](binary-table.md) que contém o bitmap ou o ícone.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Controle de imagem: ' button3 ' da caixa de diálogo: ' MyDialog ' tem os atributos icon e bitmap Set Error <br/>                                                                                                                     | Há um controle de botão de [pressão](pushbutton-control.md), [caixa de seleção](checkbox-control.md)ou de [botões de opção](radiobuttongroup-control.md) com o bit de [ícone](icon-control-attribute.md) ou o bit de [bitmap](bitmap-control-attribute.md) definido na coluna atributos da [tabela de controle](control-table.md). Você não pode definir ambos os atributos juntos.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="example"></a>Exemplo

[Tabela de controle](control-table.md) (parcial)



| caixa de diálogo\_ | Control      | Tipo             | Atributos | Propriedade     | Texto       |
|----------|--------------|------------------|------------|--------------|------------|
| MyDialog | Button1      | Botão       | 0          |              | OK         |
| MyDialog | Bitmap1      | Bitmap           | 0          |              | Bitmap1    |
| MyDialog | RadioButton1 | Botão de opção | 0          | RadioButton1 |            |
| MyDialog | ListBox1     | ListBox          | 0          | ListBox1     |            |
| MyDialog | ComboBox1    | ComboBox         | 0          | ComboBox1    |            |
| MyDialog | ListView1    | ListView         | 0          | ListView1    |            |
| MyDialog | Button2      | Botão       | 262144     |              | Bitmap2    |
| MyDialog | RadioButton2 | Botão de opção | 262144     |              | Property2  |
| MyDialog | RadioButton3 | Botão de opção | 524288     |              | Property3  |
| MyDialog | Button3      | Botão       | 786432     |              | Ambiguous1 |



 

[Tabela RadioButton](radiobutton-table.md) (parcial)



| Propriedade\_ | Ordem | Texto    |
|------------|-------|---------|
| Property2  | 1     | Bitmap3 |
| Property3  | 2     | Icon1   |



 

As tabelas a seguir estão vazias:

-   [Tabela ControlEvent,](controlevent-table.md)
-   [Tabela de ListBox](listbox-table.md)
-   [Tabela ComboBox](combobox-table.md)
-   [Tabela ListView](listview-table.md)
-   [Tabela binária](binary-table.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




