---
description: Todos os objetos de item têm propriedades.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Atributos de propriedade (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c635cb0d4e21fe2a1d65a3f21254f8e9c04d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461144"
---
# <a name="property-attributes-wia"></a>Atributos de propriedade (WIA)

Todos os objetos de item têm propriedades. As propriedades têm atributos. Por exemplo, atributos de propriedade indicam se uma propriedade é lida, gravada ou excluída. Eles também indicam os valores de propriedade válidos. As constantes a seguir são atributos de propriedade válidos: 

| Atributo de propriedade        | Significado                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| \_propproperty \_ armazenável em cache      | O dispositivo pode armazenar em cache o valor da propriedade.                                                               |
| \_sinalizador de prop WIA \_           | A propriedade tem uma lista de valores de sinalizador legais. Os valores de sinalizador são combinados por meio de uma operação **or** . |
| \_lista de propriedades do WIA \_           | A propriedade tem uma lista de valores válidos.                                                                 |
| PROP. do WIA \_ \_           | A propriedade não tem nenhum valor válido associado a ela.                                          |
| \_intervalo de prop WIA \_          | A propriedade tem um intervalo de valores válidos.                                                                |
| \_leitura de prop WIA \_           | O aplicativo pode ler o valor da propriedade.                                                           |
| \_RW prop do WIA \_             | O aplicativo pode ler e gravar o valor da propriedade.                                                 |
| sincronização de prop do WIA \_ \_ \_ necessária | Não use.                                                                                              |
| \_gravação de prop WIA \_          | O aplicativo pode gravar o valor da propriedade.                                                          |



 

 

 



