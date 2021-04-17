---
title: Diferenças entre os modelos de objeto
description: Diferenças entre os modelos de objeto
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Windows Media Player, modelo de objeto
- Modelo de objeto do Windows Media Player, diferenças de versão
- modelo de objeto, diferenças de versão
- Controle ActiveX do Windows Media Player, diferenças de versão
- Controle ActiveX, diferenças de versão
- Controle ActiveX móvel do Windows Media Player, diferenças de versão
- Windows Media Player Mobile, modelo de objeto
- Guia de migração, diferenças de versão
- versões do Windows Media Player, modelo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759724"
---
# <a name="differences-between-the-object-models"></a>Diferenças entre os modelos de objeto

Há duas diferenças principais entre o modelo de objeto do Windows Media Player 6,4 e o modelo de objeto do Windows Media Player 7 ou posterior.

-   **CLSID** do O modelo de objeto do Windows Media Player 7 ou posterior é uma partida completa do modelo de objeto da versão 6,4. A especificação de Component Object Model (COM) requer que todas as interfaces existentes continuem a funcionar em novas versões de um componente COM. Isso significa que novas interfaces podem ser adicionadas a um componente COM, mas as interfaces existentes nunca devem ser alteradas, garantindo que o código do cliente mais antigo sempre funcione com o componente específico que ele foi projetado para usar. Portanto, o controle ActiveX do Windows Media Player 7 ou posterior tem uma nova ID de classe: 6BF52A52-394A-11D3-B153-00C04F79FAA6. Se você quiser aproveitar a nova funcionalidade do controle para esta versão, você deve alterar seu CLSID.
-   **Modelo de objeto hierárquico** Se você estiver usando o controle ActiveX do Windows Media Player 6,4, talvez tenha notado que todas as propriedades, métodos e eventos são acessados por meio do mesmo objeto: o objeto **Player** . Por outro lado, o modelo de objeto do Windows Media Player 7 ou posterior é organizado como uma hierarquia de objetos. O objeto **Player** ainda é o objeto raiz, mas as funções agora são acessadas por meio de uma variedade de objetos filho.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de migração do modelo de objeto**](object-model-migration-guide.md)
</dt> </dl>

 

 




