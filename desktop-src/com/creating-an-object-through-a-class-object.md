---
title: Criando um objeto por meio de um objeto de classe
description: Criando um objeto por meio de um objeto de classe
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea76e8ecb826d8bba6e9f0ea84af894f4632d3d4bb5f41708d84c2f37e416b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993496"
---
# <a name="creating-an-object-through-a-class-object"></a>Criando um objeto por meio de um objeto de classe

Com a importância crescente das redes de computador, tornou-se necessário que clientes e servidores interajam de maneira fácil e eficiente, independentemente de residirem no mesmo computador ou em uma rede. Crucial para isso é a capacidade do cliente de iniciar um servidor, criar uma instância do objeto do servidor e ter acesso aos métodos das interfaces no objeto.

O COM fornece extensões para esse processo COM básico que o torna praticamente contínuo em uma rede. Se um cliente for capaz de identificar o servidor por meio de seu CLSID, chamar algumas funções simples permitirá que o COM faça todo o trabalho de localizar e iniciar o servidor e ativar o objeto. As sub-chaves no Registro permitem que os servidores remotos registrem sua localização, de modo que o cliente não exige essas informações. Para aplicativos que querem aproveitar os recursos de rede, as funções de criação de objeto COM permitem mais flexibilidade e eficiência.

Para obter mais informações, consulte estes tópicos:

-   [CLSIDs e objetos de classe COM](com-class-objects-and-clsids.md)
-   [Localizando um objeto remoto](locating-a-remote-object.md)
-   [Funções auxiliares de criação de instância](instance-creation-helper-functions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes e servidores COM](com-clients-and-servers.md)
</dt> </dl>

 

 




