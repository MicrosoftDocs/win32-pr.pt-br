---
description: Os aplicativos não podem ser renderizados no estéreo, a menos que o sistema operacional indique que ele permite o comportamento de exibição estereoscópico 3D. Os aplicativos determinam se devem ser renderizados em estereoscópico 3D de maneira diferente, dependendo se eles são janelas ou em tela inteira.
ms.assetid: FB8AC57E-38DD-47B5-8666-1F4B73488F8B
title: Renderização no estéreo e notificação sobre o status do estéreo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379c6335e0bd060cf0065fe92bf2ec6c086289c3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087208"
---
# <a name="rendering-in-stereo-and-notifying-about-stereo-status"></a>Renderização no estéreo e notificação sobre o status do estéreo

Os aplicativos não podem ser renderizados no estéreo, a menos que o sistema operacional indique que ele permite o comportamento de exibição estereoscópico 3D. Os aplicativos determinam se devem ser renderizados em estereoscópico 3D de maneira diferente, dependendo se eles são janelas ou em tela inteira.

Um aplicativo em janela chama o método [**IDXGIFactory2:: IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled) para determinar se deve ser renderizado em estéreo. Um aplicativo de tela inteira chama o método [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) e, em seguida, determina se algum dos modos de exibição retornados dá suporte à renderização em estéreo. O método **GetDisplayModeList1** não enumera os modos estéreo, a menos que você especifique o sinalizador estéreo de [**\_ \_ modos \_ de enumeração dxgi**](dxgi-enum-modes.md) no parâmetro *flags* . Um aplicativo com janela ou tela inteira que dá suporte a estéreo primeiro faz a determinação para renderizar em estéreo com base em uma chamada para o método **IDXGIFactory2:: IsWindowedStereoEnabled** ou **IDXGIOutput1:: GetDisplayModeList1** , respectivamente, e então registra para notificação de alterações de status de estéreo. Como o aplicativo não pode contar com a notificação para indicar o status atual do comportamento de exibição 3D estereoscópico, quando recebe um evento de notificação ou uma mensagem de janela, ele deve chamar **IDXGIFactory2:: IsWindowedStereoEnabled** ou **IDXGIOutput1:: GetDisplayModeList1** novamente para determinar o status atual do comportamento de exibição 3D de estereoscópico do sistema operacional.

Se você quiser renderizar em estéreo, deverá se registrar para notificações de estéreo para saber quando o usuário desativa ou no comportamento estéreo. Um aplicativo pode ser registrado para ser notificado sobre as alterações de status 3D do estereoscópico por meio de uma mensagem em uma janela ou por meio de sinalização de evento. Para se registrar para receber mensagens de notificação em uma janela sobre alterações de status de estéreo, um aplicativo chama o método [**IDXGIFactory2:: RegisterStereoStatusWindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow) . Para se registrar para receber a notificação de alterações de status de estéreo por meio de sinalização de evento, um aplicativo chama o método [**IDXGIFactory2:: RegisterStereoStatusEvent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent) . Os dois métodos retornam um ponteiro para um valor de chave que o aplicativo pode usar para cancelar o registro da notificação. Para cancelar o registro da notificação, o aplicativo passa esse valor de chave para o método [**IDXGIFactory2:: UnregisterStereoStatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus) .

O status do estéreo pode conter os seguintes elementos:

-   A configuração do usuário.

    Os usuários do Windows podem habilitar ou desabilitar a exibição de estéreo com a opção Habilitar estereoscópico 3D nas configurações de exibição de alteração do painel de controle.

-   A capacidade e a configuração do computador, que incluem o adaptador gráfico, o driver de gráficos e a instalação do monitor.

O [exemplo de 3D estéreo simples do Direct3D 11,1](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20stereoscopic%203D%20sample) mostra como adicionar um efeito 3D do estereoscópico e como responder às alterações do sistema estéreo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprimoramentos de DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
