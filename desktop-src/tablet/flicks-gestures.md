---
description: Windows O Vista inclui um conjunto de oito gestos de movimento básicos. Os movimentos são movimentos de caneta rápidos e lineares associados a ações de rolagem e comandos.
ms.assetid: 004c7d76-90a9-4506-a70b-dbf8f9e1c616
title: Gestos de movimentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e7d53c42eb178900ce22b7890febcfd1c6aca95f2257b0c5ed06eb20173b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936506"
---
# <a name="flicks-gestures"></a>Gestos de movimentos

Windows O Vista inclui um conjunto de oito *gestos de movimento* básicos. Os movimentos são movimentos de caneta rápidos e lineares associados a ações de rolagem e comandos.

## <a name="flick-details"></a>Detalhes do movimento

O recurso de movimentos fornece ao usuário uma nova maneira de interagir com o Tablet PC, permitindo que ações comuns sejam executadas fazendo gestos rápidos com a caneta. Os movimentos coexistem e não interrompem, ações normais do usuário, como toques à esquerda e à direita, rolagem e escrita à tinta.

Um *movimento* é um gesto de caneta unidirecional que exige que o usuário contate o digitalizador em um movimento de movimentos rápido. Um movimento é caracterizado por alta velocidade e um alto grau de reta. Um movimento é identificado pela sua direção. Os movimentos podem ser feitos em oito direções correspondentes às direções cardeal e secundária Compass.

Uma *ação ou um* *movimento* é a ação ou o atalho executado em resposta a um movimento. Os movimentos são mapeados para ações. A ilustração a seguir mostra um diagrama de oito movimentos de caneta que correspondem às suas ações de movimento.

![ilustração mostrando o mapa de gestos](images/2647eb2d-36d0-4610-b923-fa3530d1e640.jpg)

À medida que o usuário move a caneta sobre o digitalizador de um Tablet PC, o hardware gera pacotes de caneta que são roteados para o subsistema de entrada de caneta da plataforma do Tablet PC. normalmente, se a caneta estiver sendo usada como um substituto para o mouse, o subsistema de entrada de caneta usará esses pacotes de caneta e os enviará, possivelmente com modificações, a User32, o componente Windows responsável pelo processamento de entrada do mouse. Se a caneta estiver sendo usada em uma superfície de tinta, a tinta será renderizada em vez dos pacotes do mouse que estão sendo gerados.

A rotina de detecção de movimento é implementada no subsistema de entrada de caneta. A detecção de movimento começa na caneta e continua até:

1) a sequência de pacotes recebidos é determinada para não ser um movimento ou

2) a caneta é exibida.

Enquanto a detecção de movimento está ocorrendo, os pacotes de caneta são retidos e não enviados ao sistema. Isso deve ser feito porque o envio de pacotes pode interferir na ação de movimento que é executada. Por exemplo, o envio de pacotes durante um movimento que mapeia para uma ação de cópia descartará o que foi selecionado, o que significa que não haveria nada a ser copiado até a hora em que a ação foi enviada.

À medida que os pacotes fluem para o subsistema de entrada de caneta, a rotina de detecção de movimento computa métricas sobre o comprimento, a velocidade, a hora e a curvatura do movimento que está sendo executado. Com cada pacote que chega, a rotina de detecção atualiza cada uma dessas métricas. Assim que qualquer uma das métricas fica fora do que constituiria um movimento, a detecção de movimento termina e os pacotes são enviados.

## <a name="where-flicks-are-detected"></a>Onde os movimentos são detectados

Os gestos de movimento são possibilitados pelo fato de que os arrastamentos são normalmente executados com bastante lentidão. O usuário deve primeiro direcionar o ponto inicial da operação arrastar, executar o arrastar e depois direcionar o ponto de extremidade. Normalmente, isso levará muito tempo para ser qualificado como um movimento. No entanto, em superfícies de tinta, os traços rápidos que se qualificam como movimentos acontecem com frequência; cruzar um ' T' é um exemplo comum. Portanto, por padrão, a detecção de movimento é desativada sobre as superfícies de tinta e ativada em todo o sistema.

## <a name="focus-issues"></a>Problemas de foco

Depois que um movimento é detectado, uma sequência de eventos começa que, finalmente, leva ao sistema executando uma determinada ação em resposta ao movimento que ocorreu. Primeiro, a rotina de detecção no subsistema de entrada de caneta determina a qual janela o movimento deve ser enviado. Normalmente, essa é a janela que tem o foco, mas há exceções. Para movimentos de rolagem, o movimento é enviado para a janela sobre a qual ocorreu o movimento. Observe que isso não é necessariamente a janela com foco. Quando um movimento é enviado para uma janela que não tem foco, o foco não é alterado para essa janela.

## <a name="flick-actions"></a>Ações de movimento

Depois que a janela de destino for determinada, essa janela poderá lidar com o movimento em si, dependendo do comportamento de evento padrão ou programado. Os aplicativos podem responder à ação mais apropriada com base no aplicativo e na direção e posição do movimento. Por exemplo, em um aplicativo de mapeamento, movimentos para cima e para baixo podem ampliar ou reduzir em vez de rolar verticalmente, como seria esperado do comportamento padrão.

Para alertar um aplicativo de que um movimento ocorreu, uma mensagem de janela é enviada a ele. Essa mensagem de janela contém o ponto inicial do movimento e a direção do movimento. Se o aplicativo manipula essa mensagem de janela, nenhuma ação adicional é executada pelo subsistema de entrada de caneta.

Depois que um movimento é detectado, os comentários visuais que representam a ação de movimento são exibidos na tela. Esses comentários servem a duas finalidades. Primeiro, ele confirma para o usuário que o movimento foi bem-sucedido. Em segundo lugar, ele lembra ao usuário qual ação foi executada, ajudando o usuário a conectar a direção do movimento com sua ação associada.

Os comentários de movimento consistem em duas partes; um ícone que representa a ação e um rótulo que contém o nome da ação. O rótulo é exibido abaixo do ícone. Os comentários são exibidos imediatamente após a detecção do movimento. Embora os aplicativos possam personalizar seu comportamento em resposta a movimentos manipulando a mensagem de janela de movimento, o aplicativo não pode desabilitar ou modificar os comentários de movimento.

Espera-se que a maioria dos aplicativos não reconheçam o movimento e, portanto, não tratará a mensagem de janela descrita acima. Se a mensagem não for tratada, o subsistema de entrada de caneta executará uma ação adicional. Primeiro, ele pesquisa a ação associada à direção do movimento detectado. Em seguida, ele executará as etapas (descritas na tabela abaixo) para fazer com que a janela de destino Execute essa ação. Para muitas das ações de movimento, isso envolve o envio de um comando de aplicativo, mas determinadas ações implementadas não o fazem.

## <a name="processing-application-commands"></a>Processando comandos do aplicativo

Seu aplicativo deve responder a qualquer um dos comandos do aplicativo que possam ser potencialmente atribuídos a um gesto de movimento. se um aplicativo não responder à mensagem de [**\_ \_ movimento de TABLET do wm**](wm-tablet-flick-message.md), o Windows Vista seguirá enviando a notificação de [**\_ APPCOMMAND do wm**](/windows/desktop/inputdev/wm-appcommand) aplicável, seguida por uma notificação de [**\_ KEYDOWN do wm**](/windows/desktop/inputdev/wm-keydown) .

A seguir está uma lista de comandos de aplicativo que podem ser atribuídos a movimentos, com a mensagem de pressionamento de tecla de backup que pode ser enviada.



| Comando                                  | Pressionamento de tecla de backup  |
|------------------------------------------|-------------------|
| APPCOMMAND \_ navegador \_ para trás<br/> | Nenhum<br/>   |
| \_encaminhamento do navegador APPCOMMAND \_<br/>  | Nenhum<br/>   |
| \_cópia APPCOMMAND<br/>              | Ctrl+C<br/> |
| \_colar APPCOMMAND<br/>             | Ctrl+V<br/> |
| \_desfazer APPCOMMAND<br/>              | Ctrl+Z<br/> |
| APPCOMMAND \_ excluir<br/>            | Del<br/>    |
| APPCOMMAND \_ recortar<br/>               | Ctrl+X<br/> |
| APPCOMMAND \_ abrir<br/>              | Ctrl+O<br/> |
| APPCOMMAND \_ Imprimir<br/>             | Ctrl+P<br/> |
| APPCOMMAND \_ salvar<br/>              | Ctrl+S<br/> |
| APPCOMMAND \_ refazer<br/>              | Ctrl+Y<br/> |
| APPCOMMAND \_ fechar<br/>             |                   |



 

Editar comandos como copiar, colar, recortar e excluir pode ser direcionado para uma seleção ou para o objeto localizado na base do gesto de movimento. Se não houver nenhuma seleção, você poderá usar os dados na [**estrutura do \_ ponto de movimento**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) para determinar qual objeto, se houver, pode ter sido o destino do comando de edição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de API de movimentos](flicks-api-reference.md)
</dt> <dt>

[Respondendo a gestos de movimento](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

