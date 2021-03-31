---
description: Os programas de leitura de tela só podem ler o texto de um controle de botão de opção que tenha sido criado na coluna de texto da tabela RadioButton.
ms.assetid: 92ad70ec-a3a4-4ea7-8888-40c78d73e58a
title: Adicionando texto extra a botões de opção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e73ac55e300ddee603449e9ea7ce5e10f4e0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921527"
---
# <a name="adding-extra-text-to-radio-buttons"></a>Adicionando texto extra a botões de opção

Os programas de leitura de tela só podem ler o texto de um [controle de botão de opção](radiobuttongroup-control.md) que tenha sido criado na coluna de texto da [tabela RadioButton](radiobutton-table.md). Se esse texto for uma descrição insuficiente dos botões de opção, [controles de texto](text-control.md) sobrepostos poderão ser adicionados para fornecer texto descritivo extra. Esses controles de texto devem se sobrepor na caixa de diálogo e têm condições definidas na [tabela ControlCondition](controlcondition-table.md) para que apenas um controle de texto seja mostrado por vez. Os controles de texto não devem sobrepor o controle de botão de opção ou outros controles na caixa de diálogo porque isso torna os controles invisíveis para leitores de tela. Quando o usuário passa o cursor sobre o controle de texto, o programa leitor de tela lê o texto extra.

No exemplo a seguir, a caixa de diálogo MySample tem um controle de botão de opção chamado Colors com duas opções para o valor da Propriedade Color. Para cada opção, há um controle de texto com uma condição para ocultar ou mostrar, dependendo da opção atual selecionada para a cor. Um valor inicial da cor é definido na tabela de propriedades. Os controles de texto têm o texto descritivo extra criado no campo de texto da tabela RadioButton. Quando um usuário passa o cursor sobre o controle de texto na caixa de diálogo, o leitor de tela pode ler a descrição extra da opção atual.

[Tabela de diálogo](dialog-table.md)



| caixa de diálogo   | HCentering | VCentering | Largura | Altura | Atributos | Título                    | Controlar \_ primeiro | Padrão de controle \_ | \_Cancelar controle |
|----------|------------|------------|-------|--------|------------|--------------------------|----------------|------------------|-----------------|
| MySample | 50         | 50         | 200   | 180    | 3          | Botões de opção acessíveis | Cores         | Avançar             |                 |



 

[Tabela de controle](control-table.md)



| caixa de diálogo\_ | Control    | Type             | X   | S   | Largura | Altura | Atributos | Propriedade | Texto                               | \_Próximo controle | Ajuda |
|----------|------------|------------------|-----|-----|-------|--------|------------|----------|------------------------------------|---------------|------|
| MySample | Cores     | Botão de opção | 2   | 20  | 100   | 50     | 3          | A cor |                                    | Avançar          |      |
| MySample | HowIsBlue  | Texto             | 20  | 80  | 150   | 15     | 2          |          | É como o céu em um dia claro. |               |      |
| MySample | HowIsGreen | Texto             | 20  | 80  | 150   | 15     | 2          |          | É como a grama na primavera.    |               |      |



 

[Tabela de botões de opção](radiobutton-table.md)



| Propriedade | Ordem | Valor | X   | S   | Largura | Altura | Texto   | Ajuda |
|----------|-------|-------|-----|-----|-------|--------|--------|------|
| A cor | 1     | Azul  | 10  | 10  | 80    | 15     | Azul &  |      |
| A cor | 2     | Verde | 10  | 30  | 80    | 15     | &verde |      |



 

[Tabela de propriedades](property-table.md)



| Propriedade | Valor |
|----------|-------|
| A cor | Azul  |



 

[Tabela ControlCondition](controlcondition-table.md)



| caixa de diálogo\_ | controle\_  | Ação | Condição                 |
|----------|------------|--------|---------------------------|
| MySample | HowIsBlue  | Ocultar   | A cor <>  "azul"  |
| MySample | HowIsBlue  | Mostrar   | Cor = "azul"         |
| MySample | HowIsGreen | Ocultar   | A cor <>  "verde" |
| MySample | HowIsGreen | Mostrar   | Cor = "verde"        |



 

Para obter mais informações, consulte [acessibilidade](accessibility.md).

 

 



