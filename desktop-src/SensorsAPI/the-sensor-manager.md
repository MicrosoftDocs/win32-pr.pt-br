---
description: O objeto Gerenciador de sensor fornece acesso aos sensores que estão disponíveis para seu uso.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: O objeto Gerenciador de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9ce54dd72b642e599d8b7b26b8c94d1531767ec31b5ccd81a47b88746853a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117968409"
---
# <a name="the-sensor-manager-object"></a>O objeto Gerenciador de sensor

O objeto Gerenciador de sensor fornece acesso aos sensores que estão disponíveis para seu uso.

Para usar a API do sensor, você deve primeiro chamar o método COM **CoCreateInstance** para criar uma instância do objeto do sensor Manager e recuperar um ponteiro para sua interface, chamada [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager). O Gerenciador de sensor mantém a lista de sensores disponíveis. Você pode usar **ISensorManager** para chamar métodos que recuperam grupos de sensores por categoria ou por tipo, ou você pode chamar um método para recuperar um sensor específico usando sua ID exclusiva. O Gerenciador de sensor também permite que você se registre para receber um evento que notifica quando um novo sensor está conectado à plataforma.

Às vezes, o Gerenciador de sensor fornece um ponteiro para um sensor, mas o usuário não habilitou o sensor. Por exemplo, geralmente é possível recuperar valores para propriedades de sensor não particulares, como o fabricante ou modelo do sensor, antes que o usuário habilite o sensor. Essas informações podem ajudá-lo a decidir se deseja solicitar ao usuário a permissão para usar o sensor. Você pode chamar [**ISensorManager:: RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) para solicitar que o usuário habilite um sensor específico ou uma coleção de sensores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando permissões de usuário](managing-user-permissions.md)
</dt> <dt>

[Solicitando permissões de usuário](requesting-user-permissions.md)
</dt> </dl>

 

 
