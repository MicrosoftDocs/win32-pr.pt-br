---
title: Estilos de controle de animação (CommCtrl. h)
description: Esta seção lista os estilos de janela usados com controles de animação.
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aff6116433533bdc79535be0e282cb81baa9368f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470618"
---
# <a name="animation-control-styles"></a>Estilos de controle de animação

Esta seção lista os estilos de janela usados com controles de animação.




| Constante | Descrição | 
|----------|-------------|
| <span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl><dt><strong>ACS_AUTOPLAY</strong></dt></dl> | Começa a reproduzir a animação assim que o clipe AVI é aberto. <br /> | 
| <span id="ACS_CENTER"></span><span id="acs_center"></span><dl><dt><strong>ACS_CENTER</strong></dt></dl> | Centraliza a animação na janela do controle de animação. <br /> | 
| <span id="ACS_TIMER"></span><span id="acs_timer"></span><dl><dt><strong>ACS_TIMER</strong></dt></dl> | Por padrão, o controle cria um thread para reproduzir o clipe AVI. Se você definir esse sinalizador, o controle reproduzirá o clipe sem criar um thread; internamente, o controle usa um temporizador do Win32 para sincronizar a reprodução. <br /><strong>Comctl32.dll versão 6 e posterior:</strong> Não há suporte para esse estilo. Por padrão, o controle reproduz o clipe AVI sem criar um thread.<br /><blockquote>[!Note]<br />Comctl32.dll versão 6 não é redistribuível. Para usar Comctl32.dll versão 6, especifique-o em um manifesto. Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.</blockquote><br /> | 
| <span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl><dt><strong>ACS_TRANSPARENT</strong></dt></dl> | Permite que você coincida a cor do plano de fundo de uma animação com a da janela subjacente, criando um plano de fundo "transparente". O pai do controle de animação não deve ter o estilo de WS_CLIPCHILDREN (consulte <a href="/windows/desktop/winmsg/window-styles">estilos de janela</a>). O controle envia uma mensagem de <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> para seu pai. Use <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> para definir a cor do plano de fundo para o contexto do dispositivo como um valor apropriado. O controle interpreta o pixel superior esquerdo do primeiro quadro como a cor de fundo padrão da animação. Ele remapeará todos os pixels com essa cor para o valor que você forneceu em resposta a WM_CTLCOLORSTATIC. <br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



