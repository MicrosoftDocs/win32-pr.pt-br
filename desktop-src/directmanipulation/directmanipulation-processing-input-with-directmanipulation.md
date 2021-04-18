---
description: Esta seção fornece uma visão geral do modelo de threading de manipulação direta, como as mensagens de janela são processadas pela manipulação direta e como o estado de um visor é alterado como entrada é mapeado para os movimentos de saída.
ms.assetid: 0818E34E-990E-4C36-9954-EF87EB226AF6
title: Processando a entrada com DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 284a0a1866a2082e2c34c65de347b0dcdfab3a64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105773928"
---
# <a name="processing-input-with-directmanipulation"></a>Processando a entrada com DirectManipulation

Esta seção fornece uma visão geral do modelo de threading de [manipulação direta](direct-manipulation-portal.md) , como as mensagens de janela são processadas pela manipulação direta e como o estado de um visor é alterado como entrada é mapeado para os movimentos de saída.

- [Fluxo de entrada](#input-flow)
- [Comentários](#remarks)

A [manipulação direta](direct-manipulation-portal.md) usa dois threads para coordenar operações assíncronas:

*Thread de interface do usuário* -o thread que possui o **HWND** associado à entrada. Esse thread possui inicialização de [manipulação direta](direct-manipulation-portal.md). O processamento de entrada do mouse e do teclado também ocorre no thread da interface do usuário.

*Delegue thread* -o thread criado e de propriedade da [manipulação direta](direct-manipulation-portal.md). O processamento de entrada por toque ocorre no thread delegado.

## <a name="input-flow"></a>Fluxo de entrada

Em uma configuração típica em que o teste de clique é feito no thread da interface do usuário, as mensagens de janela são processadas pela [manipulação direta](direct-manipulation-portal.md) na seguinte ordem:

![diagrama que mostra a ordem na qual as mensagens são processadas.](images/inputprocessing.png)

Para um visor em repouso:

1. Uma série de mensagens do Windows alcança o thread delegado.
2. As mensagens de [WM_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) são enviadas pelo thread delegado para o thread de teste de clique independente (IHT).
3. Se [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) for chamado a partir do thread IHT, as mensagens poderão ser enviadas ao thread da interface do usuário pelo thread delegado, dependendo do valor [**do \_ \_ tipo DIRECTMANIPULATION HITTEST**](/windows/win32/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type) quando [**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget) for chamado.
4. Se [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) não for chamado a partir do thread IHT, as mensagens serão sempre enviadas pelo thread delegado para o thread da interface do usuário.
5. O cliente pode chamar [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) do thread da interface do usuário para permitir que a [manipulação direta](direct-manipulation-portal.md) detecte uma manipulação.
6. Se uma manipulação for detectada, a [manipulação direta](direct-manipulation-portal.md) enviará uma mensagem do [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) para notificar o cliente de que a entrada está sendo tratada pela manipulação direta. O status do visor é definido como **em execução** e a transformação saída será atualizada.
7. Se uma interação diferente de uma manipulação for detectada, a [manipulação direta](direct-manipulation-portal.md) enviará as mensagens restantes para o thread da interface do usuário.

Para um visor em movimento (com um status de em execução ou inércia), a mensagem de janela alcança o thread delegado primeiro, em que a [manipulação direta](direct-manipulation-portal.md) faz testes em todas as viewports em execução. A manipulação direta atribui automaticamente o contato para as viewports apropriadas identificadas pelo teste de clique. O status do visor está em execução e a transformação saída será atualizada.

Em alguns casos, um thread de interface do usuário do aplicativo pode estar muito lento para responder a testes de clique. Um thread de teste de clique pode ser usado ([**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)) para permitir que o cliente mova o [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e as mensagens de [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) para um thread específico para permitir o teste de clique.

## <a name="remarks"></a>Comentários

Normalmente, a [manipulação direta](direct-manipulation-portal.md) envia somente mensagens do [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) ao thread da interface do usuário, recolocando mensagens posteriores enquanto aguarda uma resposta do cliente. Se o cliente chamar [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact), as únicas mensagens que o thread da interface do usuário recebe quando uma manipulação é detectada são o [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e o [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md)e a [mensagem do WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md).

O cliente pode não chamar [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) ao processar mensagens do [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) e [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) . Nesse caso, a [manipulação direta](direct-manipulation-portal.md) envia todas as mensagens para o thread da interface do usuário sem analisar as mensagens para ver se há uma manipulação. Em seguida, o cliente pode escolher qualquer ponto para chamar **setcontact** e fazer com que a manipulação direta comece a detectar manipulações e envie mensagens de [mensagem do WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) quando uma for detectada.

**Windows 10 e posterior:** Você pode decidir quais manipulações deseja manipular chamando [**DeferContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact) antes de chamar [**setcontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) em uma mensagem do [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) ou [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) . **DeferContact** garante que todas as mensagens subsequentes sejam enviadas ao thread da interface do usuário pelo período de tempo especificado.
