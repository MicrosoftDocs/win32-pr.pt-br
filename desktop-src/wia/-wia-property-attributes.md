---
description: Todos os objetos de item têm propriedades.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Atributos de propriedade (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdee1cdee48bba6183f9bcae2abc521ac9f53dfb33eec544ab3ed6bead4947b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007526"
---
# <a name="property-attributes-wia"></a>Atributos de propriedade (WIA)

Todos os objetos de item têm propriedades. As propriedades têm atributos. Por exemplo, atributos de propriedade indicam se uma propriedade é lida, escrita ou excluída. Eles também indicam os valores de propriedade válidos. As constantes a seguir são atributos de propriedade válidos: 

| Atributo property        | Significado                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| WIA \_ PROP \_ CACHEABLE      | O dispositivo pode armazenar em cache o valor da propriedade.                                                               |
| SINALIZADOR WIA \_ PROP \_           | A propriedade tem uma lista de valores de sinalizador legal. Os valores de sinalizador são combinados usando uma **operação OR bit** a bit. |
| WIA \_ PROP \_ LIST           | A propriedade tem uma lista de valores legais.                                                                 |
| WIA \_ PROP \_ NONE           | A propriedade não tem nenhum valor válido associado a ela.                                          |
| INTERVALO DE PROP DO WIA \_ \_          | A propriedade tem um intervalo de valores válidos.                                                                |
| WIA \_ PROP \_ READ           | O aplicativo pode ler o valor da propriedade.                                                           |
| WIA \_ PROP \_ RW             | O aplicativo pode ler e gravar o valor da propriedade.                                                 |
| SINCRONIZAÇÃO \_ WIA PROP \_ \_ NECESSÁRIA | Não use.                                                                                              |
| WIA \_ PROP \_ WRITE          | O aplicativo pode gravar o valor da propriedade.                                                          |



 

 

 



