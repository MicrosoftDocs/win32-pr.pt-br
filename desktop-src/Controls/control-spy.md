---
title: Controle Spy v 2.0
description: O Spy Control é uma ferramenta que ajuda os desenvolvedores a entenderem os controles comuns como aplicar estilos a eles e como eles respondem a mensagens e notificações.
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104008532"
---
# <a name="control-spy-v20"></a>Controle Spy v 2.0

O Spy Control é uma ferramenta que ajuda os desenvolvedores a entenderem os controles comuns: como aplicar estilos a eles e como eles respondem a mensagens e notificações. Usando o espião de controle, você pode ver imediatamente como os estilos diferentes afetam o comportamento e a aparência de cada controle e também como você pode alterar o estado de cada controle enviando mensagens.

Duas versões do Control Spy estão disponíveis, uma para [Comctl32.dll versão 5. x](common-control-versions.md) e outra para Comctl32.dll versão 6,0 e posterior. ControlSpyV6.exe tem um manifesto de aplicativo interno para que ele use os controles mais recentes, com tema. ControlSpyV5.exe não tem esse manifesto e, por isso, o padrão é a versão mais antiga.

Este tópico inclui as seções a seguir.

-   [Visão geral](#overview)
-   [Estilos](#styles)
-   [Mensagens](#messages)
-   [Tamanho/cor](#sizecolor)
-   [Onde obter o espião de controle](#where-to-get-control-spy)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

O Spy de controle hospeda um controle comum selecionado no centro de sua janela de aplicativo. Você pode alterar qual controle é mostrado selecionando controles diferentes na caixa de listagem no lado esquerdo da janela. As mensagens ou notificações recebidas pelo controle serão listadas no lado direito da janela à medida que chegarem. Você pode habilitar ou desabilitar essa funcionalidade usando as caixas de seleção **mensagens recebidas** e **notificações recebidas** .

A imagem a seguir mostra o aplicativo do Spy Control.

![janela do Spy Control](images/controlspy-main.png)

Na parte inferior da janela, há várias guias que apresentam mais funcionalidade.

## <a name="styles"></a>Estilos

A guia **estilos** permite que você altere o estilo da janela atual do controle. Selecione ou desmarque qualquer um dos estilos listados e, em seguida, clique no botão **aplicar** para alterar o estilo do controle exibido. Como alternativa, você pode usar o botão **recriar** para criar um novo controle com os estilos selecionados. O botão **Redefinir** retornará o controle para os estilos padrão.

Os botões **copiar estilo** e **Copiar do filestyle** abaixo da guia copiarão as constantes de estilo selecionadas para a área de transferência como uma lista de bits ou ( \| ) delimitadas. Você pode colar essa lista diretamente em sua chamada para [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para fornecer um controle em seu próprio aplicativo com o mesmo estilo.

A imagem a seguir mostra a guia **estilos** de um controle de botão.

![guia estilos do Spy Control](images/controlspy-styles.png)

## <a name="messages"></a>Mensagens

A guia **mensagens** permite que você envie quase qualquer mensagem a um controle. Depois de selecionar uma mensagem na caixa de listagem, você pode inserir dados que são enviados como os parâmetros *wParam* e *lParam* da chamada para [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage). Depois de clicar em **Enviar**, a mensagem é enviada ao controle e qualquer resultado é exibido na caixa de texto na parte inferior da guia.

A imagem a seguir mostra a guia mensagens quando uma determinada mensagem é selecionada.

![guia Mensagens do Spy Control](images/controlspy-messages.png)

## <a name="sizecolor"></a>Tamanho/cor

A guia **tamanho/cor** pode ser usada para alterar o tamanho do controle, bem como a cor de seu plano de fundo.

## <a name="where-to-get-control-spy"></a>Onde obter o espião de controle

Você pode baixar o [Control Spy 2,0](https://www.microsoft.com/download/details.aspx?id=4635) do MSDN. Ambas as versões estão contidas no download.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Controles do Windows](window-controls.md)
</dt> <dt>

[Habilitar estilos visuais](cookbook-overview.md)
</dt> </dl>

 

 