---
title: A função named_type_to_local
description: Os stubs chamam o \_ tipo nomeado \_ para \_ função local para converter dados de um tipo transmitido para o tipo que eles apresentam para o aplicativo.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fc1d45545c920ef19eb4c230045e62322833d3ef38e765357c29b20a48589c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924056"
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

 

 




