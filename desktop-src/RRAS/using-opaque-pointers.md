---
title: Usando ponteiros opacos
description: Os clientes geralmente devem armazenar informações adicionais específicas do cliente sobre destinos.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d24524f64fca7062ffb35ed6f4d5e6a2bc935ef7fee0c7fa141cb2e823e70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025066"
---
# <a name="using-opaque-pointers"></a>Usando ponteiros opacos

Os clientes geralmente devem armazenar informações adicionais específicas do cliente sobre destinos. O gerenciador de tabela de roteamento permite que os clientes armazenem essas informações em estruturas de destino na tabela de roteamento. As informações são armazenadas e recuperadas usando *ponteiros opacos*. As informações armazenadas são privadas e acessíveis somente para o cliente que possui o ponteiro opaco.

Por exemplo, o gerenciador de grupos multicast mantém uma lista de entradas de encaminhamento multicast que dependem de um destino específico. O gerenciador de grupos multicast usa um ponteiro opaco nesse destino. Em outro exemplo, um protocolo de roteamento que anuncia um destino específico pode manter informações relacionadas a seu próprio anúncio de rota do destino usando um ponteiro opaco, mesmo que ele não tenha a melhor rota.

O número de ponteiros opacos é limitado; esses ponteiros são alocados aos clientes por primeira vez. O administrador do roteador deve alocar o número correto de ponteiros durante a configuração do roteador; portanto, os protocolos de roteamento e outros clientes devem documentar o uso de ponteiros opacos.

 

 




