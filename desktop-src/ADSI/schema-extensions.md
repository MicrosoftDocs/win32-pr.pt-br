---
title: Extensões de esquema
description: A arquitetura do esquema ADSI fornece que novas classes de esquema podem ser adicionadas ao contêiner de classes de esquema e novas propriedades a um objeto de classe de esquema existente em tempo de execução.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7fdc4b363fea83029fc5526464bd5825fa851dbe82e874911a0ab45d869843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178815"
---
# <a name="schema-extensions"></a>Extensões de esquema

A arquitetura do esquema ADSI fornece que novas classes de esquema podem ser adicionadas ao contêiner de classes de esquema e novas propriedades a um objeto de classe de esquema existente em tempo de execução. A última capacidade não requer nenhum código novo. Esse é um recurso importante para namespaces que permitem serviços de diretório extensível. O componente do provedor deve permitir essa extensibilidade e saber onde acessar e armazenar a instância de classe e os valores de suas propriedades. Em um serviço de diretório extensível típico, essas informações são armazenadas no banco de dados do serviço de diretório da mesma maneira que qualquer outra classe de esquema e definições de propriedade.

> [!Note]  
> Na terminologia da interface COM, somente as propriedades podem ser adicionadas a uma classe de esquema existente, não a métodos. Adicionar um novo método exigiria adicionar uma nova implementação desse método e, portanto, exigir código adicional.

 

Para obter um exemplo de um esquema de provedor específico, consulte [Gerenciamento de esquema](schema-management.md).

 

 




