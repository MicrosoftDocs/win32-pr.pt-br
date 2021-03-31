---
title: Como funcionam as propriedades
description: Como funcionam as propriedades
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Plug-ins do Windows Media Player, propriedades de exemplo de eco
- plug-ins, propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, propriedades de exemplo de eco
- Plug-ins do DSP, propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636256"
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

 

 




