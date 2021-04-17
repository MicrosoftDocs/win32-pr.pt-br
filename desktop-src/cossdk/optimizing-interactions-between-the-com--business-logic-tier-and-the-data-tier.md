---
description: A camada de dados geralmente contém informações mais estáticas&\# 8212; informações mantidas na mídia durável.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Otimizar chamadas entre os dados e a lógica de negócios do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765659"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a>Otimização de interações entre a camada de lógica de negócios COM+ e a camada de dados

A camada de dados geralmente contém principalmente informações estáticas – informações mantidas em mídia durável. Como essa camada abrange informações que são principalmente estáticas, ela requer uma análise completa para possíveis afunilamentos. Além da possibilidade óbvia de gargalos de conexão, os pontos de acesso podem ser causados por registros acessados com frequência, métodos ineficientes para acessar dados e a necessidade de coordenar o acesso a sistemas herdados.

## <a name="connecting-to-the-data-tier"></a>Conectando-se à camada de dados

Duas considerações desempenham um papel importante na criação de uma camada de dados para um aplicativo COM+: pooling de conexões e [ativação JIT (just-in-time) com+](com--just-in-time-activation.md)e o uso de DSNs. Os componentes que fazem conexões com a camada de dados devem usar o conjunto de [pools de objetos com+](com--object-pooling.md) no componente.

Ao criar DSNs, use as cadeias de caracteres de construtor de objeto especificadas no componente em vez de criar um DSN de arquivo. Os DSNs de arquivo são mais lentos que uma conexão usando uma cadeia de caracteres de construtor de objeto. As cadeias de caracteres do construtor de objetos podem ser especificadas na folha de propriedades do componente. Para obter mais informações, consulte [cadeias de caracteres do construtor de objeto com+](com--object-constructor-strings.md).

Se você estiver usando componentes para acessar um banco de dados SQL Server, use o pool de objetos COM+ em vez do pool de conexões SQL.

Se o componente estiver usando o ADO para buscar vários conjuntos de registros, estabeleça várias conexões para o componente. Quando o ADO recupera vários conjuntos de registros, ele cria várias conexões em segundo plano se você não criá-las. Se você criá-los, poderá agrupá-los e ter mais controle sobre o número de conexões usadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Otimização de interações entre a camada de lógica de negócios COM+ e a camada de apresentação](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



