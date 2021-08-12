---
title: Interface IWMPControls2 (VB e C) (Wmp.h)
description: Fornece um método que complementa a interface IWMPControls.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- Interface IWMPControls2 (VB e C ) Windows Media Player
- Interface IWMPControls2 (VB e C ) Windows Media Player , descrita
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9757471526eb385168a10c505254b5a418ea7f9811576de95266c06817c73109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575916"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a>Interface IWMPControls2 (VB e C#)

Fornece um método que complementa a interface [**IWMPControls.**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)

## <a name="members"></a>Membros

A interface **IWMPControls2 (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMPControls2 (VB e C#)** tem esses métodos.



| Método                                                           | Descrição                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Passo**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | Move o item de mídia de vídeo atual para o próximo quadro ou o quadro anterior e congela a reprodução.<br/> |



 

O código de exemplo a seguir mostra como acessar uma interface [**IWMPControls2.**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) O código de exemplo lança o [**valor IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) que a propriedade [**AxWindowsMediaPlayer.Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) retorna para um **valor IWMPControls2.**

Para **C#:**


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



Para **VB:**


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Iwmpcontrols**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





