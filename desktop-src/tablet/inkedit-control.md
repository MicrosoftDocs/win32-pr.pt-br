---
description: O controle InkEdit fornece uma maneira fácil de capturar, reconhecer e exibir tinta.
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: Controle InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa64c4452ba5d7f66cdc03a1148c02a12f3945f876d68ac240ff4473e8d50bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451317"
---
# <a name="inkedit-control"></a>Controle InkEdit

O controle [InkEdit](inkedit-control-reference.md) fornece uma maneira fácil de capturar, reconhecer e exibir tinta.

Essa implementação do controle [InkEdit](inkedit-control-reference.md) é baseada no controle [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) . a implementação gerenciada (.NET Framework) de [InkEdit](/previous-versions/ms835842(v=msdn.10)) é baseada no controle [**RichTextBox**](/previous-versions/windows/) .

A principal finalidade do controle [InkEdit](inkedit-control-reference.md) é coletar tinta, reconhecê-la e exibi-la em formato de texto. Além disso, ele dá suporte à exibição de tinta como um objeto incorporado com recursos de formatação de texto, como negrito e sublinhado.

## <a name="gestures-and-correction"></a>Gestos e correção

[InkEdit](inkedit-control-reference.md) dá suporte aos seguintes gestos.



| Gesto                                                                    | Nome do gesto              | Ação               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![gesto para baixo à esquerda](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | Para baixo à esquerda<br/>      | Digite<br/>     |
| ![gesto para baixo-esquerdo-longo](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | Para baixo à esquerda-longa<br/> | Digite<br/>     |
| ![gesto para cima para a direita](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | Para cima à direita<br/>       | Tab<br/>       |
| ![gesto de cima para a direita.](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | Para cima à direita<br/>  | Tab<br/>       |
| ![gesto direito](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | Direita<br/>          | Space<br/>     |
| ![gesto esquerdo](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | Esquerda<br/>           | Backspace<br/> |



 

Os eventos de gesto que você pode manipular contêm informações de gesto, traço e cursor que podem ser usadas para enviar texto para [InkEdit](inkedit-control-reference.md) ou inserir dados na área de transferência.

[InkEdit](inkedit-control-reference.md) também fornece uma interface do usuário de correção que permite que os usuários exibam e selecionem alternativas, usem o teclado na tela e os reconhecedores de caractere/letra/bloco.

## <a name="other-details"></a>Outros detalhes

[InkEdit](inkedit-control-reference.md) foi projetado para funcionar bem em um cenário de formulário para uma única linha, bem como entrada e edição de texto multilinha. O uso pretendido principal para InkEdit é obter entrada de texto de um usuário na forma de manuscrito. Por padrão, a entrada de tinta é reconhecida e o texto é inserido em seu lugar. A interface do usuário padrão para InkEdit é semelhante à do controle [**RichTextBox**](/previous-versions/windows/) , exceto quando o usuário está fazendo o layout da tinta. Você pode exibir a tinta original em vez de texto; no entanto, a tinta é dimensionada para o tamanho da fonte de entrada atual do controle InkEdit e é exibida embutida com outro texto.

> [!Note]  
> Por motivos de segurança, você deve usar os procedimentos padrão para abrir ou fechar um arquivo, transmitir a entrada/saída e definir a propriedade [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) ou [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) .

 

O controle [InkEdit](inkedit-control-reference.md) é definido para reconhecer tinta como texto por padrão. Para permitir que os usuários adicionem tinta como tinta, defina a propriedade [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) como **InsertAsInk**.

Para obter informações de referência detalhadas sobre o controle [InkEdit](inkedit-control-reference.md) , consulte InkEdit.

> [!Note]  
> Se você usar o controle do Win32 [InkEdit](inkedit-control-reference.md) e colocá-lo dentro de uma caixa de grupo, verifique se a caixa tem um estilo transparente; caso contrário, InkEdit não será capaz de coletar tinta.

 

> [!Note]  
> Para garantir que a tinta seja exibida corretamente, chame o método de [**atualização**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) de controle [InkEdit](inkedit-control-reference.md) quando receber um evento [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) ou [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) .

 

As seções a seguir detalham o uso do controle [InkEdit](inkedit-control-reference.md) :

-   [Instanciando InkEdit](instantiating-inkedit.md)
-   [Reconhecimento de palavra versus caractere](word-vs--character-recognition.md)
-   [Exibindo tinta como tinta](displaying-ink-as-ink.md)
-   [Usando InkEdit em versões anteriores do Windows](using-inkedit-on-earlier-versions-of-windows.md)
-   [Usando um dicionário de aplicativo com InkEdit](using-an-application-dictionary-with-inkedit.md)

 

