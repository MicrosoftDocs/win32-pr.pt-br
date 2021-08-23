---
description: As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um dos gestos de caneta listados é detectado.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Visualização de caneta (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60b9f75493a361cc167b65fba1783bc01f909d76211b1076e2faccc2e6f00116
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548486"
---
# <a name="pen-visualization"></a>Visualização de caneta

As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um dos gestos de caneta listados é detectado.

Essas constantes são usadas com os parâmetros **SPI \_ GETPENVISUALIZATION** e **SPI \_ SETPENVISUALIZATION** e a [**função SystemParametersInfo.**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)

<dl> <dt>

<span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZAÇÃO \_ OFF**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Especifica que os comentários da interface do usuário para todos os gestos de caneta estão desligados.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION \_ ON**
</dt> <dd> <dl> <dt>

0x0023
</dt> <dt>



Especifica que os comentários da interface do usuário para todos os gestos de caneta estão ativas.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION \_ TAP**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Especifica os comentários da interface do usuário para um toque de caneta.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**DOUBLETAP DE \_ PENVISUALIZAÇÃO**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Especifica os comentários da interface do usuário para um toque duplo de caneta.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**CURSOR DE \_ PENVISUALIZAÇÃO**
</dt> <dd> <dl> <dt>

0x0020
</dt> <dt>



Especifica os comentários da interface do usuário para o cursor de caneta.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de configuração](configuration-constants.md)
</dt> <dt>

[**Visualização de contato**](contact-visualization.md)
</dt> <dt>

[**Systemparametersinfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configuração de comentários de entrada](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

