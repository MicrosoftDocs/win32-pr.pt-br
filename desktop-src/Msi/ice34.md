---
description: O ICE34 valida que cada botão de opção em cada controle do grupo de botões tem uma propriedade na coluna propriedade da tabela RadioButton que especifica seu grupo de botões de opção.
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755083"
---
# <a name="ice34"></a>ICE34

O ICE34 valida que cada botão de opção em cada controle do grupo de [botões](radiobuttongroup-control.md) tem uma propriedade na coluna propriedade da [tabela RadioButton](radiobutton-table.md) que especifica seu grupo de botões de opção. ICE34 valida que essa propriedade existe e é definida como um valor padrão na tabela de [Propriedades](property-table.md) , que é igual a um dos valores de botão de opção do grupo na coluna valor da tabela RadioButton.

Um grupo de botões de opção deve ter um padrão para que os usuários possam selecionar uma opção usando a tecla TAB. Isso é necessário para a acessibilidade adequada do usuário.

ICE34 relata tabelas ausentes.

## <a name="result"></a>Resultado

ICE34 postar uma mensagem de erro se houver um botão de opção que especifique uma propriedade inválida.

## <a name="example"></a>Exemplo

ICE34 relata os erros a seguir para o exemplo mostrado.



| Erro de ICE34                                                                                                                                                                | Descrição                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Control caixa de diálogo. Control2 deve ter uma propriedade porque é do tipo RadioButton.                                                                                      | Há um controle de grupo de [botões](radiobuttongroup-control.md), sem o bit de [controle indireto](indirect-control-attribute.md) definido na coluna atributos da [tabela de controle](control-table.md), que não tem uma propriedade listada na coluna propriedade. |
| Talvez não seja um valor padrão válido para o messagebutton usando a propriedade Property3. O valor deve ser listado como uma opção na tabela de botão de opção.                 | Há um valor padrão para uma propriedade especificada na coluna valor da [tabela de propriedades](property-table.md) que não é um dos valores para o grupo de botões de opção especificado na coluna valor da [tabela RadioButton](radiobutton-table.md).                  |
| A propriedade PropertyB deve ser definida porque é uma propriedade indireta de um controle de botão de caixa de diálogo. Control4                                                       | A propriedade referenciada por este grupo de botões de opção é uma propriedade indireta e o valor da propriedade indireta não é uma das opções para o grupo de botões de opção.                                                                                                       |
| Talvez não seja um valor padrão válido para a propriedade propertya. A propriedade é uma propriedade do botão de opção indireto do controle dialogo. Control5 (via Propriedade Property5). | O valor da propriedade indireta referenciada por meio do controle não é um dos valores padrão para esse botão de opção.                                                                                                                                                    |



 

[Tabela de controle](control-table.md) (parcial)



| caixa de diálogo  | Control  | Tipo             | Atributos | Propriedade  |
|---------|----------|------------------|------------|-----------|
| Caixa de diálogo | Control1 | Botão de opção | 0          | Property1 |
| Caixa de diálogo | Control2 | Botão de opção | 0          |           |
| Caixa de diálogo | Control3 | Botão de opção | 0          | Property3 |
| Caixa de diálogo | Control4 | Botão de opção | 8          | Property4 |
| Caixa de diálogo | Control5 | Botão de opção | 8          | Property5 |



 

[Tabela de propriedades](property-table.md) (parcial)



| Propriedade  | Valor     |
|-----------|-----------|
| Property1 | Yes       |
| Property3 | Talvez     |
| Property4 | PropertyB |
| Property5 | Propriedade |
| Propriedade | Talvez     |



 

[Tabela RadioButton](radiobutton-table.md) (parcial)



| Propriedade  | Ordem | Valor |
|-----------|-------|-------|
| Property1 | 1     | Sim   |
| Property1 | 2     | Agora   |
| Property2 | 1     | Sim   |
| Property2 | 2     | Não    |
| Property3 | 1     | Sim   |
| Property3 | 2     | Não    |
| Property4 | 1     | Sim   |
| Property4 | 2     | Não    |
| Propriedade | 1     | Sim   |
| Propriedade | 2     | Não    |
| PropertyB | 1     | Sim   |
| PropertyB | 2     | Não    |



 

Para corrigir os erros relatados por este ICE, verifique o seguinte:

-   Que cada entrada de controle RadioButton sem o conjunto de atributos indiretos tem uma propriedade listada na coluna Propriedade:
-   Cada propriedade desse tipo tem pelo menos uma entrada correspondente na tabela RadioButton.
-   Que cada propriedade desse tipo é definida na tabela de propriedades, com um valor que é uma das opções da tabela RadioButton.
-   Que cada propriedade referenciada na coluna Property de um controle RadioButton com o conjunto de atributos indiretos é definida na tabela de propriedades.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



