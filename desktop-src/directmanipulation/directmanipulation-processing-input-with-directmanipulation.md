---
description: Esta seção fornece uma visão geral do modelo de threading de Manipulação Direta, como as mensagens de janela são processadas pela Manipulação Direta e como o estado de um viewport muda conforme a entrada é mapeada para os movimentos de saída.
ms.assetid: 0818E34E-990E-4C36-9954-EF87EB226AF6
title: Processamento de entrada com DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 49b72f88da8978192af402c8b810655c102395d5aad273f34340ed57e2703008
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094646"
---
# <a name="processing-input-with-directmanipulation"></a>Processamento de entrada com DirectManipulation

Esta seção fornece uma visão geral do modelo de [threading](direct-manipulation-portal.md) de Manipulação Direta, como as mensagens de janela são processadas pela Manipulação Direta e como o estado de um viewport muda conforme a entrada é mapeada para os movimentos de saída.

- [Fluxo de entrada](#input-flow)
- [Comentários](#remarks)

[A Manipulação](direct-manipulation-portal.md) Direta usa dois threads para coordenar operações assíncronas:

*Thread de interface do* usuário – o thread que possui **o HWND** associado à entrada. Esse thread possui a inicialização da [Manipulação Direta.](direct-manipulation-portal.md) O processamento de entrada do mouse e do teclado também acontece no thread da interface do usuário.

*Delegar thread* – o thread criado e pertencente à [Manipulação Direta.](direct-manipulation-portal.md) O processamento de entrada por toque ocorre no thread delegado.

## <a name="input-flow"></a>Fluxo de entrada

Em uma configuração típica em que o teste de acerto [](direct-manipulation-portal.md) é feito no thread da interface do usuário, as mensagens da janela são processadas pela Manipulação Direta na seguinte ordem:

![diagrama mostrando a ordem na qual as mensagens são processadas.](images/inputprocessing.png)

Para um viewport em repouso:

1. Uma série de mensagens de janela atinge o thread delegado.
2. [WM_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) mensagens são enviadas pelo thread delegado para o thread IHT (Teste de Acerto Independente).
3. Se [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) for chamado do thread IHT, as mensagens poderão ser enviadas ao thread da interface do usuário pelo thread delegado, dependendo do valor de [**DIRECTMANIPULATION \_ HITTEST \_ TYPE**](/windows/win32/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type) quando [**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget) foi chamado.
4. Se [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) não for chamado do thread IHT, as mensagens sempre serão enviadas pelo thread delegado para o thread da interface do usuário.
5. O cliente pode chamar [**SetContact do**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) thread da interface do usuário para permitir que a [Manipulação Direta](direct-manipulation-portal.md) detecte uma manipulação.
6. Se uma manipulação for [detectada,](direct-manipulation-portal.md) a Manipulação Direta enviará uma mensagem [wm/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) para notificar o cliente de que a entrada está sendo manipulada pela Manipulação Direta. O status do viewport é definido como **RUNNING** e a transformação de saída será atualizada.
7. Se uma interação diferente de uma manipulação for detectada, a [Manipulação](direct-manipulation-portal.md) Direta enviará mensagens restantes para o thread da interface do usuário.

Para um viewport em movimento (com o status RUNNING ou INERTIA), [](direct-manipulation-portal.md) a mensagem da janela atinge o thread delegado primeiro, em que a Manipulação Direta faz testes de acerto em todos os viewports em execução. A Manipulação Direta atribui automaticamente o contato aos viewports apropriados identificados pelo teste de impacto. O status do viewport é RUNNING e a transformação de saída será atualizada.

Em alguns casos, um thread de interface do usuário do aplicativo pode ser muito lento para responder a testes de ocorrência. Um thread de teste de ocorrência pode ser usado ([**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)) para permitir que o cliente mova mensagens [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) para um thread específico para permitir testes de ocorrência.

## <a name="remarks"></a>Comentários

Normalmente, [](direct-manipulation-portal.md) a Manipulação Direta envia apenas [mensagens WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) [e DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) para o thread da interface do usuário, retendo mensagens posteriores enquanto aguarda uma resposta do cliente. Se o cliente chamar [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact), as únicas mensagens recebidas pelo thread da interface do usuário quando uma manipulação for detectada serão [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md)e [mensagem WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md).

O cliente pode não chamar [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) ao processar [mensagens WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) [e DM/_POINTERHITTEST.](../inputmsg/dm-pointerhittest.md) Nesse caso, a [Manipulação Direta](direct-manipulation-portal.md) envia todas as mensagens para o thread da interface do usuário sem analisar as mensagens para ver se há uma manipulação. O cliente pode escolher qualquer ponto para chamar **SetContact** e fazer com que a Manipulação Direta comece a detectar manipulações e envie mensagens [wm/_POINTERCAPTURECHANGED mensagem](../inputmsg/wm-pointercapturechanged.md) quando uma for detectada.

**Windows 10 e posterior:** Você pode decidir quais manipulações deseja manipular chamando [**DeferContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact) antes de chamar [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) em uma mensagem [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) ou [DM/_POINTERHITTEST.](../inputmsg/dm-pointerhittest.md) **DeferContact** garante que todas as mensagens subsequentes sejam enviadas para o thread da interface do usuário pelo período de tempo especificado.
