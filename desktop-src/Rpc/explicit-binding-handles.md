---
title: Identificadores de associação explícitos
description: Para obter o controle máximo sobre o processo de associação, os aplicativos cliente/servidor podem usar identificadores de ligação explícitos.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b391c339ac3747928e3394152e9c0de7c1c7aa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754298"
---
# <a name="explicit-binding-handles"></a>Identificadores de associação explícitos

Para obter o controle máximo sobre o processo de associação, os aplicativos cliente/servidor podem usar identificadores de ligação explícitos. Como os identificadores implícitos, os identificadores de ligação explícitos permitem que o aplicativo cliente selecione um servidor para executar suas chamadas. Além disso, os identificadores de ligação explícitos permitem que o aplicativo cliente/servidor crie uma sessão de comunicação RPC autenticada. Com identificadores explícitos, o cliente pode se conectar a mais de um servidor e executar procedimentos remotos em vários servidores. Aplicativos cliente multithread e assíncronos podem até mesmo se conectar a vários servidores e executar vários procedimentos remotos ao mesmo tempo.

Seu aplicativo cliente deve passar o identificador explícito como um parâmetro para cada chamada de procedimento remoto. Para estar de acordo com o padrão uso, o identificador deve ser especificado como o primeiro parâmetro em cada procedimento remoto. No entanto, as extensões da Microsoft para RPC permitem que você especifique o identificador de associação em outras posições. Para obter mais informações, consulte [extensões de Binding-Handle RPC da Microsoft](microsoft-rpc-binding-handle-extensions.md).

Para criar um identificador explícito, declare o identificador como um parâmetro para as operações remotas no arquivo IDL. O [exemplo Hello, World](tutorial.md) pode ser redefinido para usar um identificador explícito, conforme mostrado:

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

Você pode combinar identificadores explícitos e implícitos em uma única interface. Se uma função tiver um identificador explícito em sua lista de parâmetros, esse identificador será usado. Se uma função em uma interface que usa identificadores implícitos não especificar um identificador explícito, o identificador implícito padrão será usado.

 

 




