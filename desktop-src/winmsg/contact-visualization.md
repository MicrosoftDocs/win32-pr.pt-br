---
description: As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um contato de entrada é detectado.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Visualização de contato (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea196017b1731bb176cd21a7dc02aaa360f4fe70503bd204b9c488d38eff99ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437249"
---
# <a name="contact-visualization"></a>Visualização de contato

As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um contato de entrada é detectado.

Essas constantes são usadas com os parâmetros **SPI \_ GETCONTACTVISUALIZATION** e **SPI \_ SETCONTACTVISUALIZATION** e a [**função SystemParametersInfo.**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)

<dl> <dt>

<span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ OFF**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Especifica que os comentários da interface do usuário para todos os contatos estão desligados.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_ ON**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Especifica os comentários da interface do usuário para todos os contatos.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION \_ PRESENTATIONMODE**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Especifica que os comentários da interface do usuário para todos os contatos estão em com visuais de modo de apresentação.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de configuração](configuration-constants.md)
</dt> <dt>

[**Visualização de gestos**](gesture-visualization.md)
</dt> <dt>

[**Systemparametersinfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configuração de comentários de entrada](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

