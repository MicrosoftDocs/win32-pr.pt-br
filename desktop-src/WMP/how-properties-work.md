---
title: Como funcionam as propriedades
description: Como funcionam as propriedades
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- plug-ins Windows Media Player, propriedades de exemplo de eco
- plug-ins, propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, propriedades de exemplo de eco
- Plug-ins do DSP, propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdefea3fce39b70d20d2f100d36cc4aeb8770bd15cd5cd0bf0978cd08f2259f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339130"
---
# <a name="how-properties-work"></a>Como funcionam as propriedades

Os valores de propriedade são armazenados em variáveis de membro.

As propriedades tornam-se acessíveis por pares de métodos. Um método fornece a implementação para especificar o valor da propriedade; seu nome começa com Put \_ . O outro método fornece a implementação para recuperar o valor da propriedade; seu nome começa com get \_ . A definição de interface está em Echo. idl. Os protótipos do método de propriedade estão em Echo. h. Eles são implementados em Echo. cpp.

As próximas três seções mostrarão como modificar os métodos de propriedade existentes para atender às suas necessidades e como adicionar os métodos para uma propriedade adicional.

-   [Variáveis para armazenar propriedades](variables-to-store-properties.md)
-   [Modificando a propriedade Scale](modifying-the-scale-property.md)
-   [Adicionando a propriedade de combinação úmida](adding-the-wet-mix-property.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedades de exemplo de eco**](echo-sample-properties.md)
</dt> </dl>

 

 




