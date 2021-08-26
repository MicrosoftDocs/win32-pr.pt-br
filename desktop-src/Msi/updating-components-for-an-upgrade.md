---
description: Por design, os usuários do produto MNP2000 fictício nunca devem usar arquivos atualizados, como Baseba01.txt.
ms.assetid: 5aca7ff5-c09f-4d00-b319-2b89550686ab
title: Atualizando componentes para uma atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e725653acc7aadbeb3710d3cd6b1ee6dc2971e51d3583f2be279ddfed008d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039236"
---
# <a name="updating-components-for-an-upgrade"></a>Atualizando componentes para uma atualização

Por design, os usuários do produto MNP2000 fictício nunca devem usar arquivos atualizados, como Baseba01.txt. portanto, os arquivos atualizados são por definição incompatível com o produto original e os componentes de Windows Installer, como beisebol, que contém esses arquivos, devem receber novos códigos de componentes. Novos arquivos, como Opera01.txt, são introduzidos como parte de um novo componente com um código de componente exclusivo. como o produto original e a atualização usam o mesmo componente Bloco de notas, o código do componente desse componente não é alterado. Para obter mais informações sobre quando o código do componente deve ser alterado, consulte [alterando o código do componente](changing-the-component-code.md).

Use o Orca ou outro editor de banco de dados para inserir os dados a seguir na [tabela de componentes](component-table.md) de MNP2001.msi. Não reutilize os GUIDs mostrados abaixo na coluna ComponentID no seu exemplo.

[Tabela de componentes](component-table.md)



| Componente  | ComponentId                            | Diretório\_ | Atributos | Condição | KeyPath      |
|------------|----------------------------------------|-------------|------------|-----------|--------------|
| Beisebol   | {2951190A-6AF8-4D7F-AA16-D256405C277A} | SPORTDIR    | 2          |           | Baseba01.txt |
| Quadra | {E1AAB6B0-FEC6-4F18-B765-3B05A81CEACB} | SPORTDIR    | 2          |           | Basket01.txt |
| Concerto    | {C28C5064-AA84-4431-AC69-FC1321DF18AF} | ARTSDIR     | 2          |           | Concer01.txt |
| Dance      | {1AC2B14D-D5F4-4642-9F7A-EE81BF59B3E2} | ARTSDIR     | 2          |           | Dance01.txt  |
| Opera      | {C2DABF7E-1EF6-458D-84B1-AAC1127CED26} | ARTSDIR     | 2          |           | Opera01.txt  |
| Comemorar   | {92AA30F4-7AC5-4DFA-801E-988CF3DAA4DC} | SPORTDIR    | 2          |           | Footba01.txt |
| Ajuda       | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| Janeiro    | {E90CD0E6-ED8D-4F88-B000-27BD2B482C6C} | MONDIR      | 2          |           | Janua01.txt  |
| NewYears   | {1EEF8C53-F7C0-405C-8FE3-2B0FE54B0114} | HOLDIR      | 2          |           | NewYea01.txt |
| Memorial   | {BA81ACF7-4D43-424F-93B0-8845A2DF1C02} | HOLDIR      | 2          |           | Memori01.txt |
| Bloco de notas    | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

[Continuar](updating-features-for-an-upgrade.md)

 

 



