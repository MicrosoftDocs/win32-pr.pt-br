---
description: A tabela ReserveCost é uma tabela opcional que permite que o autor Reserve uma quantidade de espaço em disco em qualquer diretório que dependa do estado de instalação de um componente.
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: Tabela ReserveCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df729e6afd66222bed3025991432354a7ec04023dcba17ce2bc5b5d81788827b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990399"
---
# <a name="reservecost-table"></a>Tabela ReserveCost

A tabela ReserveCost é uma tabela opcional que permite que o autor Reserve uma quantidade de espaço em disco em qualquer diretório que dependa do estado de instalação de um componente.

A tabela ReserveCost tem as colunas a seguir.



| Coluna        | Tipo                               | Chave | Nullable |
|---------------|------------------------------------|-----|----------|
| ReserveKey    | [Identificador](identifier.md)       | Y   | N        |
| Componente\_   | [Identificador](identifier.md)       | N   | N        |
| ReserveFolder | [Identificador](identifier.md)       | N   | Y        |
| ReserveLocal  | [DoubleInteger](doubleinteger.md) | N   | N        |
| Conservar | [DoubleInteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey
</dt> <dd>

Chave primária que identifica exclusivamente uma entrada de tabela ReserveCost.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa para a coluna um da tabela de [componentes](component-table.md) . Reserva uma quantidade especificada de espaço se este componente deve ser instalado.

</dd> <dt>

<span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder
</dt> <dd>

Esta coluna contém o nome de uma propriedade que é o caminho completo para o diretório de destino. Esse nome de propriedade normalmente é o nome de um diretório na tabela de [diretório](directory-table.md) ou o nome de um conjunto de propriedades obtido usando a ação [Appsearch](appsearch-action.md) . Isso adiciona a quantidade de espaço em disco especificada em ReserveLocal ou o inserve para o custo de volume do dispositivo que contém o diretório.

</dd> <dt>

<span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal
</dt> <dd>

O número de bytes de espaço em disco a ser reservado se o componente vinculado estiver instalado para ser executado localmente.

</dd> <dt>

<span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>Conservar
</dt> <dd>

O número de bytes de espaço em disco a ser reservado se o componente vinculado estiver instalado para ser executado da origem.

</dd> </dl>

## <a name="remarks"></a>Comentários

Reservar custos dessa maneira pode ser útil para autores que desejam garantir que uma quantidade mínima de espaço em disco estará disponível depois que a instalação for concluída. Por exemplo, esse espaço em disco pode ser reservado para documentos de usuário ou para arquivos de aplicativo (como arquivos de índice) que são criados somente depois que o aplicativo é iniciado após a instalação.

Você pode usar a tabela ReserveCost para habilitar ações personalizadas para especificar um custo aproximado para quaisquer arquivos, entradas de registro ou outros itens que a ação personalizada possa instalar. As ações personalizadas que adicionam entradas à tabela ReserveCost devem ser sequenciadas entre as ações [CostInitialize](costinitialize-action.md) e [filecost](filecost-action.md) . Isso é necessário para a ação filecost inicializar corretamente o custo de todos os componentes afetados pelas entradas na tabela ReserveCost.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



