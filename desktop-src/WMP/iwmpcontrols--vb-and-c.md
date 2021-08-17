---
title: Interface IWMPControls (VB e C ) (Wmp.h)
description: Fornece uma maneira de manipular a reprodução de um item de mídia representando os controles de transporte do Windows Media Player, como Reproduzir, Parar e Pausar. A interface IWMPControls expõe as propriedades a seguir.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- Interface IWMPControls (VB e C) Windows Media Player
- Interface IWMPControls (VB e C ) Windows Media Player , descrita
topic_type:
- apiref
api_name:
- IWMPControls (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b96f79b8942935d9722bf38dbd1ae946b03d16496664b4c069552819785c1f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119305"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a>Interface IWMPControls (VB e C#)

Fornece uma maneira de manipular a reprodução de um item de mídia representando os controles de transporte do Windows Media Player, como Reproduzir, Parar e Pausar.

A interface **IWMPControls** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPControls (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPControls (VB e C#)** tem esses métodos.



| Método                                                                       | Descrição                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Fastforward**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | Inicia a reprodução rápida do item de mídia na direção da frente.<br/>                     |
| [**fastReverse**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | Inicia a reprodução rápida do item de mídia na direção inversa.<br/>                     |
| [**Próximo**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | Define o próximo item na playlist como o item atual.<br/>                          |
| [**Pausa**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | Pausa a reprodução do item de mídia.<br/>                                               |
| [**Jogar**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | Inicia a reprodução do item de mídia atual ou retoma a reprodução de um item em pausa.<br/> |
| [**playItem**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | Reproduz o item de mídia especificado.<br/>                                                  |
| [**Anterior**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | Define o item anterior na playlist como o item atual.<br/>                      |
| [**Parar**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | Interrompe a reprodução do item de mídia.<br/>                                                |



 

### <a name="properties"></a>Propriedades

A interface **IWMPControls (VB e C#)** tem essas propriedades.



| Propriedade                                                                                                    | Tipo de acesso           | Descrição                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Currentitem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | Leitura/gravação<br/> | Obtém ou define o item de mídia atual em uma playlist.<br/>                                                                                                                    |
| [**Currentmarker**](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define o número do marcador atual.<br/>                                                                                                                               |
| [**Currentposition**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | Leitura/gravação<br/> | Obtém ou define a posição atual no item de mídia em segundos desde o início.<br/>                                                                                    |
| [**currentPositionString**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | Somente leitura<br/>  | Obtém a posição atual no item de mídia como **um System.String.**<br/>                                                                                                   |
| [**Isavailable**](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | Somente leitura<br/>  | Obtém um valor que indica se um tipo especificado de informações está disponível ou se uma ação especificada pode ser executada. Em C#, esse é o **método \_ get isAvailable.**<br/> |



 

Obter uma interface **IWMPControls** usando a propriedade a seguir.



| Objeto                                                                   | Propriedade                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPControls2 (VB e C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





