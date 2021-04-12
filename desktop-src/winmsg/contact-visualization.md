---
description: As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um contato de entrada é detectado.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Visualização de contato (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297287"
---
# <a name="contact-visualization"></a>Visualização de contato

As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um contato de entrada é detectado.

Essas constantes são usadas com os parâmetros **SPI \_ GETCONTACTVISUALIZATION** e **SPI \_ SETCONTACTVISUALIZATION** e a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

<dl> <dt>

<span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ desativado**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Especifica comentários da interface do usuário para todos os contatos está desativado.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_ em**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Especifica os comentários da interface do usuário para todos os contatos está ativado.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION \_ presentationmode**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Especifica os comentários da interface do usuário para todos os contatos estão ativados com visuais do modo de apresentação.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de configuração](configuration-constants.md)
</dt> <dt>

[**Visualização do gesto**](gesture-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configuração de comentários de entrada](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

