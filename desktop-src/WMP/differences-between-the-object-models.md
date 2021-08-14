---
title: Diferenças entre os modelos de objeto
description: Diferenças entre os modelos de objeto
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Windows Media Player, modelo de objeto
- modelo de objeto Windows Media Player, diferenças de versão
- modelo de objeto, diferenças de versão
- controle de ActiveX de Windows Media Player, diferenças de versão
- controle de ActiveX, diferenças de versão
- Windows Media Player controle de ActiveX móvel, diferenças de versão
- Windows Media Player Móvel, modelo de objeto
- Guia de migração, diferenças de versão
- versões do Windows Media Player, modelo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dd3b7862e2d9c5580950ad2eb718bd1c8125a5d22ec6a08533c140de545086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749737"
---
# <a name="differences-between-the-object-models"></a>Diferenças entre os modelos de objeto

há duas diferenças principais entre o modelo de objeto Windows Media Player 6,4 e o modelo de objeto Windows Media Player 7 ou posterior.

-   **CLSID** do o modelo de objeto Windows Media Player 7 ou posterior é uma partida completa do modelo de objeto da versão 6,4. A especificação de Component Object Model (COM) requer que todas as interfaces existentes continuem a funcionar em novas versões de um componente COM. Isso significa que novas interfaces podem ser adicionadas a um componente COM, mas as interfaces existentes nunca devem ser alteradas, garantindo que o código do cliente mais antigo sempre funcione com o componente específico que ele foi projetado para usar. portanto, o controle ActiveX Windows Media Player 7 ou posterior tem uma nova ID de classe: 6BF52A52-394A-11D3-B153-00C04F79FAA6. Se você quiser aproveitar a nova funcionalidade do controle para esta versão, você deve alterar seu CLSID.
-   **Modelo de objeto hierárquico** se você estiver usando o controle de ActiveX Windows Media Player 6,4, talvez tenha notado que todas as propriedades, métodos e eventos são acessados por meio do mesmo objeto: o objeto **Player** . por outro lado, o modelo de objeto Windows Media Player 7 ou posterior é organizado como uma hierarquia de objetos. O objeto **Player** ainda é o objeto raiz, mas as funções agora são acessadas por meio de uma variedade de objetos filho.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de migração do modelo de objeto**](object-model-migration-guide.md)
</dt> </dl>

 

 




