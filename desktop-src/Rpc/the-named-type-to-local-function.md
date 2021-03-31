---
title: A função named_type_to_local
description: Os stubs chamam o \_ tipo nomeado \_ para \_ função local para converter dados de um tipo transmitido para o tipo que eles apresentam para o aplicativo.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cbdd01ea657408b1bf355f41b3b9dfba673a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005517"
---
# <a name="the-named_type_to_local-function"></a>O \_ tipo nomeado \_ para \_ função local

Os stubs chamam **o \_ tipo nomeado \_ para função \_ local** para converter dados de um tipo transmitido para o tipo que eles apresentam para o aplicativo. A função é definida como:

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

O primeiro parâmetro aponta para os dados transmitidos. A função define o segundo parâmetro para apontar para os dados apresentados.

O **\_ tipo nomeado \_ para função \_ local** deve gerenciar memória para o tipo apresentado. A função deve alocar memória para toda a estrutura de dados iniciada no endereço indicado pelo segundo parâmetro, exceto pelo próprio parâmetro (o stub aloca memória para o nó raiz e a transmite para a função). O valor do segundo parâmetro não pode ser alterado durante a chamada. A função pode alterar o conteúdo nesse endereço.

 

 




