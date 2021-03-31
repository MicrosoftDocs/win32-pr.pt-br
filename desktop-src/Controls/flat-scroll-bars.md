---
title: Barras de rolagem simples
description: O Microsoft Internet Explorer 4,0 introduziu uma nova tecnologia Visual chamada barras de rolagem simples.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fbbdb64aa9815cb56f5dc3bf55ffb17390db38
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641889"
---
# <a name="flat-scroll-bars"></a>Barras de rolagem simples

O Microsoft Internet Explorer 4,0 introduziu uma nova tecnologia Visual chamada barras de rolagem simples. Funcionalmente, barras de rolagem simples se comportam exatamente como barras de rolagem padrão. A diferença é que você pode personalizar sua aparência para uma extensão maior do que as barras de rolagem padrão.

A ilustração a seguir mostra uma janela que contém uma barra de rolagem simples.

![captura de tela de uma janela que contém uma barra de rolagem simples](images/flatsb.jpg)

> [!Note]  
> As barras de rolagem simples têm suporte em Comctl32.dll versões 4,71 a 5,82. Comctl32.dll versões 6, 0 e posteriores não dão suporte a barras de rolagem simples.

 

## <a name="using-flat-scroll-bars"></a>Usando barras de rolagem simples

Esta seção descreve como implementar barras de rolagem simples em seu aplicativo.

### <a name="before-you-begin"></a>Antes de começar

Para usar as funções da barra de rolagem simples, você deve incluir commctrl. h em seus arquivos de origem e vincular com o Comctl32. lib.

### <a name="adding-flat-scroll-bars-to-a-window"></a>Adicionando barras de rolagem simples a uma janela

Para adicionar barras de rolagem simples a uma janela, chame [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passando o identificador para a janela. Em vez de usar as funções da barra de rolagem padrão para manipular suas barras de rolagem, você deve usar a função equivalente do FlatSB \_ xxx. Há funções de barra de rolagem simples para configurar e recuperar as informações de rolagem, o intervalo e a posição. Se as barras de rolagem simples não tiverem sido inicializadas para a sua janela, a API da barra de rolagem simples adiará as funções padrão correspondentes, se alguma for usada. Isso permite ativar e desativar barras de rolagem simples sem a necessidade de escrever código condicional.

Como um aplicativo pode ter definido métricas personalizadas para suas barras de rolagem simples, eles não são atualizados automaticamente quando as métricas do sistema são alteradas. Quando a métrica da barra de rolagem do sistema é alterada, uma mensagem do [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) é transmitida, com o *wParam* definido como [**SPI \_ SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). Para atualizar as barras de rolagem simples para as novas métricas do sistema, os aplicativos devem lidar com essa mensagem e alterar explicitamente as propriedades dependentes da métrica da barra de rolagem plana.

Para atualizar suas propriedades da barra de rolagem, use [**FlatSB \_ SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop). O fragmento de código a seguir altera as propriedades dependentes da métrica de uma barra de rolagem plana para os valores atuais do sistema.


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

[**FlatSB \_ O SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) permite que você modifique as barras de rolagem simples para personalizar a aparência da janela. Para barras de rolagem vertical, você pode alterar a largura da barra e a altura das setas de direção. Para barras de rolagem horizontais, você pode alterar a altura da barra e a largura das setas de direção. Você também pode alterar a cor da tela de fundo das barras de rolagem horizontal e vertical.

[**FlatSB \_ O SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) também permite que você personalize como as barras de rolagem simples são exibidas. Alterando as propriedades do WSB \_ prop \_ VSTYLE e do WSB \_ prop \_ HSTYLE, você pode definir o tipo de barra de rolagem que deseja usar. Três estilos estão disponíveis.



|                    |                                                                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_modo de encartamento de FSB \_ | Uma barra de rolagem plana padrão é exibida. Quando o mouse se move sobre um botão de direção ou o polegar, essa parte da barra de rolagem será exibida em 3-D.             |
| \_modo simples de FSB \_    | Uma barra de rolagem plana padrão é exibida. Quando o mouse se move sobre um botão de direção ou o polegar, essa parte da barra de rolagem será exibida em cores invertidas. |
| \_modo regular do FSB \_ | Uma barra de rolagem normal e não plana é exibida. Nenhum efeito visual especial será aplicado.                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a>Removendo barras de rolagem simples

Se você quiser remover barras de rolagem simples de sua janela, chame a função [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) , passando o identificador para a janela. Essa função remove apenas as barras de rolagem simples da janela em tempo de execução. Você não precisa chamar essa função quando sua janela é destruída.

 

 