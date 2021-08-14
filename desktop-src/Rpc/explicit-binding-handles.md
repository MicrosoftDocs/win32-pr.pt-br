---
title: Alças de associação explícitas
description: Para controle máximo sobre o processo de associação, os aplicativos cliente/servidor podem usar alças de associação explícitas.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a6e723d8559dc5e72783412eb6250f69431f31d08a92c4984fb2e2a19b761d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930015"
---
# <a name="explicit-binding-handles"></a>Alças de associação explícitas

Para controle máximo sobre o processo de associação, os aplicativos cliente/servidor podem usar alças de associação explícitas. Assim como os alças implícitos, os alças de associação explícita permitem que seu aplicativo cliente selecione um servidor para executar suas chamadas. Além disso, os alças de associação explícita permitem que seu aplicativo cliente/servidor crie uma sessão de comunicação RPC autenticada. Com alças explícitas, o cliente pode se conectar a mais de um servidor e executar procedimentos remotos em vários servidores. Aplicativos cliente multithread e assíncronos podem até mesmo se conectar a vários servidores e executar vários procedimentos remotos ao mesmo tempo.

O aplicativo cliente deve passar o handle explícito como um parâmetro para cada chamada de procedimento remoto. Para estar em conformidade com o padrão OSF, o handle deve ser especificado como o primeiro parâmetro em cada procedimento remoto. No entanto, as extensões da Microsoft para RPC permitem que você especifique o alça de associação em outras posições. Para obter mais informações, consulte [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).

Para criar um handle explícito, declare o handle como um parâmetro para as operações remotas no arquivo IDL. O [exemplo Hello, World](tutorial.md) pode ser redefinido para usar um handle explícito, conforme mostrado:

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

Você pode combinar alças explícitas e implícitas em uma única interface. Se uma função tiver um alçado explícito em sua lista de parâmetros, esse manipular será usado. Se uma função em uma interface usando alças implícitas não especificar um handle explícito, o handle implícito padrão será usado.

 

 




