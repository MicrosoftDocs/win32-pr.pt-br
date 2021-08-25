---
title: Barras de rolagem simples
description: O Microsoft Internet Explorer 4.0 introduziu uma nova tecnologia visual chamada barras de rolagem simples.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24a89479ffc5bae08ed08f5c3f0ca2ec9498ac781438708154ca503a2427ffc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799637"
---
# <a name="flat-scroll-bars"></a>Barras de rolagem simples

O Microsoft Internet Explorer 4.0 introduziu uma nova tecnologia visual chamada barras de rolagem simples. Funcionalmente, as barras de rolagem simples se comportam como barras de rolagem padrão. A diferença é que você pode personalizar sua aparência em uma extensão maior do que as barras de rolagem padrão.

A ilustração a seguir mostra uma janela que contém uma barra de rolagem simples.

![captura de tela de uma janela que contém uma barra de rolagem simples](images/flatsb.jpg)

> [!Note]  
> As barras de rolagem simples têm suporte Comctl32.dll versões 4.71 a 5.82. Comctl32.dll versões 6.00 e posteriores não são suportadas barras de rolagem simples.

 

## <a name="using-flat-scroll-bars"></a>Usando barras de rolagem simples

Esta seção descreve como implementar barras de rolagem simples em seu aplicativo.

### <a name="before-you-begin"></a>Antes de começar

Para usar as funções de barra de rolagem simples, você deve incluir Commctrl.h em seus arquivos de origem e vincular com Comctl32.lib.

### <a name="adding-flat-scroll-bars-to-a-window"></a>Adicionando barras de rolagem simples a uma janela

Para adicionar barras de rolagem simples a uma janela, chame [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passando o alça para a janela. Em vez de usar as funções de barra de rolagem padrão para manipular suas barras de rolagem, você deve usar a função EQUIVALENTE flatSB \_ XXX. Há funções de barra de rolagem simples para definir e recuperar as informações de rolagem, o intervalo e a posição. Se as barras de rolagem simples não foram inicializadas para sua janela, a API da barra de rolagem simples adiará para as funções padrão correspondentes, se alguma for usada. Isso permite ativar e desativar barras de rolagem simples sem precisar escrever código condicional.

Como um aplicativo pode ter definido métricas personalizadas para suas barras de rolagem simples, elas não são atualizadas automaticamente quando as métricas do sistema mudam. Quando as métricas da barra de rolagem do sistema mudam, uma mensagem [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) é transmitida, com seu *wParam* definido como [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). Para atualizar barras de rolagem simples para as novas métricas do sistema, os aplicativos devem manipular essa mensagem e alterar explicitamente as propriedades dependentes de métrica da barra de rolagem simples.

Para atualizar as propriedades da barra de rolagem, use [**FlatSB \_ SetScrollProp.**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) O fragmento de código a seguir altera as propriedades dependentes de métrica de uma barra de rolagem simples para os valores atuais do sistema.


```
void FlatSB_UpdateMetrics(HWND hWnd)
{
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXVSCROLL, GetSystemMetrics(SM_CXVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHSCROLL, GetSystemMetrics(SM_CXHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVSCROLL, GetSystemMetrics(SM_CYVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYHSCROLL, GetSystemMetrics(SM_CYHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHTHUMB, GetSystemMetrics(SM_CXHTHUMB), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVTHUMB, GetSystemMetrics(SM_CYVTHUMB), TRUE);
}
```



### <a name="enhancing-flat-scroll-bars"></a>Aprimorando barras de rolagem simples

[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) permite modificar as barras de rolagem simples para personalizar a aparência da janela. Para barras de rolagem verticais, você pode alterar a largura da barra e a altura das setas de direção. Para barras de rolagem horizontais, você pode alterar a altura da barra e a largura das setas de direção. Você também pode alterar a cor da tela de fundo das barras de rolagem horizontais e verticais.

[**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) também permite personalizar como as barras de rolagem simples são exibidas. Alterando as propriedades WSB PROP VSTYLE e \_ \_ WSB \_ PROP HSTYLE, você pode definir o tipo de barra de rolagem \_ que deseja usar. Três estilos estão disponíveis.



|   Estilo                 |   Descrição                                                                                                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODO ENCARTA FSB \_ \_ | Uma barra de rolagem simples padrão é exibida. Quando o mouse se move sobre um botão de direção ou o polegar, essa parte da barra de rolagem será exibida em 3D.             |
| MODO SIMPLES \_ FSB \_    | Uma barra de rolagem simples padrão é exibida. Quando o mouse se move sobre um botão de direção ou o polegar, essa parte da barra de rolagem será exibida em cores invertidas. |
| MODO \_ REGULAR \_ FSB | Uma barra de rolagem normal e não desfiada é exibida. Nenhum efeito visual especial será aplicado.                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a>Removendo barras de rolagem simples

Se você quiser remover barras de rolagem simples da janela, chame a [**função UninitializeFlatSB,**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) passando o alça para a janela. Essa função remove apenas barras de rolagem simples da janela em tempo de executar. Você não precisa chamar essa função quando a janela for destruída.

 

 