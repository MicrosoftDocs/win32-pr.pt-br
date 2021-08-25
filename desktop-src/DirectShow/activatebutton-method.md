---
description: O método ActivateButton ativa o botão de menu selecionado.
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: Método ActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64853a191f688758deb42061e95c91308ff88c00fe9482cce677f8b00926f26f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873516"
---
# <a name="activatebutton-method"></a>Método ActivateButton

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O método ActivateButton ativa o botão de menu selecionado.

``` syntax
        MSWebDVD.ActivateButton()
```

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.

Use este método para ativar um botão que foi selecionado por meio do método [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md)ou [**SelectRightButton**](selectrightbutton-method.md) .

 

 



