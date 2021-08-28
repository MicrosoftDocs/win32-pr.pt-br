---
description: A camada de dados geralmente contém principalmente informações estáticas&\# 8212;informações persistentes na mídia durável.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Otimizar chamadas entre a lógica de negócios e os dados COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66427f1f3761a27dc6828735ca04d98a1ca2accaaa549453c8219482cdfdabc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070406"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a>Otimizando interações entre a camada lógica de negócios COM+ e a camada de dados

A camada de dados geralmente contém principalmente informações estáticas – informações persistentes na mídia durável. Como essa camada abrange informações que são principalmente estáticas, ela requer uma análise completa para possíveis gargalos. Além da possibilidade óbvia de gargalos de conexão, os pontos de acesso podem ser causados por registros acessados com frequência, métodos de acesso a dados ineficientes e a necessidade de coordenar o acesso a sistemas herdados.

## <a name="connecting-to-the-data-tier"></a>Conectando-se à camada de dados

Duas considerações desempenham um papel importante na criação de uma camada de dados para um aplicativo COM+: o pool de conexões e a ativação [JIT (Just-In-Time)](com--just-in-time-activation.md)do COM+ e o uso de DSNs. Os componentes que fazem conexões com a camada de dados devem usar o [conjunto de pools de](com--object-pooling.md) objetos COM+ no componente.

Ao criar DSNs, use cadeias de caracteres de construtor de objeto especificadas no componente em vez de criar um DSN de arquivo. Os DSNs de arquivo são mais lentos do que uma conexão usando uma cadeia de caracteres do construtor de objeto. As cadeias de caracteres do construtor de objeto podem ser especificadas na folha de propriedades do componente. Para obter mais informações, consulte [Cadeias de caracteres do construtor de objeto COM+.](com--object-constructor-strings.md)

Se você estiver usando componentes para acessar um banco de SQL Server, use o pool de objetos COM+ em vez de SQL pool de conexões.

Se o componente estiver usando o ADO para buscar vários registros, estabeleça várias conexões para o componente. Quando o ADO recupera vários registros, ele cria várias conexões em segundo plano se você não as cria. Se você os criar, poderá em pool deles e ter mais controle sobre o número de conexões usadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Otimizando interações entre a camada lógica de negócios COM+ e a camada de apresentação](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



