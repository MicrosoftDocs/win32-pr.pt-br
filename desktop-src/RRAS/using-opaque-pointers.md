---
title: Usando ponteiros opacos
description: Geralmente, os clientes devem armazenar informações adicionais específicas do cliente sobre os destinos.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9893b3a8b8e8a69ab78f33156efbe872b86d83ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822826"
---
# <a name="using-opaque-pointers"></a>Usando ponteiros opacos

Geralmente, os clientes devem armazenar informações adicionais específicas do cliente sobre os destinos. O Gerenciador de tabela de roteamento permite que os clientes armazenem essas informações em estruturas de destino na tabela de roteamento. As informações são armazenadas e recuperadas usando *ponteiros opacos*. As informações armazenadas são privadas e acessíveis somente para o cliente que possui o ponteiro opaco.

Por exemplo, o Gerenciador de grupos de multicast mantém uma lista de entradas de encaminhamento de multicast que dependem de um destino específico. O Gerenciador do grupo de multicast usa um ponteiro opaco nesse destino. Em outro exemplo, um protocolo de roteamento que anuncia um destino específico pode manter informações relacionadas ao seu próprio anúncio de rota do destino usando um ponteiro opaco, mesmo que ele não tenha a melhor rota.

O número de ponteiros opacos é limitado; Esses ponteiros são alocados aos clientes de acordo com a primeira vez que são atendidos. O administrador do roteador deve alocar o número correto de ponteiros durante a configuração do roteador; Portanto, os protocolos de roteamento e outros clientes devem documentar o uso de ponteiros opacos.

 

 




