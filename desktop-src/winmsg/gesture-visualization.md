---
description: As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um dos gestos listados é detectado.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Visualização do gesto (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f572addf2ad7a98dbe3afc63c69a305ea15546e9533918d952271372cf52b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849815"
---
# <a name="gesture-visualization"></a>Visualização do gesto

As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um dos gestos listados é detectado.

Essas constantes são usadas com os parâmetros **SPI \_ GETGESTUREVISUALIZATION** e **SPI \_ SETGESTUREVISUALIZATION** e a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

**Observação**  

Para recuperar ou definir informações de visualização da caneta, recomendamos que você use os parâmetros **SPI \_ GETPENVISUALIZATION** e **SPI \_ SETPENVISUALIZATION** e as constantes listadas na [**visualização de caneta**](pen-visualization.md).

<dl> <dt>

<span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ desativado**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Especifica que os comentários da interface do usuário para todos os gestos estão desativados.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_ em**
</dt> <dd> <dl> <dt>

0x001F
</dt> <dt>



Especifica que os comentários da interface do usuário para todos os gestos estão ativados.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**\_toque GESTUREVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Especifica comentários da interface do usuário para um toque.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Especifica comentários da interface do usuário para um toque duplo.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION \_ PRESSANDTAP**
</dt> <dd> <dl> <dt>

0x0004
</dt> <dt>



Especifica comentários da interface do usuário para uma operação pressionar e tocar.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION \_ PRESSANDHOLD**
</dt> <dd> <dl> <dt>

0x0008
</dt> <dt>



Especifica os comentários da interface do usuário para uma operação de pressionar e manter pressionado.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION \_ RIGHTTAP**
</dt> <dd> <dl> <dt>

0x0010
</dt> <dt>



Especifica comentários da interface do usuário para um toque à direita.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de configuração](configuration-constants.md)
</dt> <dt>

[**Visualização de contato**](contact-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configuração de comentários de entrada](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

