---
title: Sobre cursores
description: Este tópico discute os cursores padrão.
ms.assetid: 0ca8e51c-1159-47e9-ba3f-5ced0667cadb
keywords:
- resources,cursors
- cursores, sobre
- cursores, padrão
- cursores padrão
- Função SetSystemCursor
- cursores, personalizados
- cursores personalizados
- cursores, pontos de calor
- cursores, criando
- criando cursores
- cursores, localização
- cursores, aparência
- destruir cursores
- duplicando cursores
- cursor de classe
- limitando cursores
- cursores, destruidor
- cursores, duplicando
- cursores, classe
- cursores, limitando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8d987eb12857779ac85d34cb7e4ff7f3f5ce59ed8a750764c433c88abbccea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735364"
---
# <a name="about-cursors"></a>Sobre cursores

Windows fornece um conjunto de cursores padrão que estão disponíveis para qualquer aplicativo usar a qualquer momento. Os arquivos de título do SDK contêm identificadores para os cursores padrão– os identificadores começam com o **prefixo IDC. \_**

Cada cursor padrão tem uma imagem padrão correspondente associada. O usuário ou um aplicativo pode substituir a imagem padrão associada a qualquer cursor padrão a qualquer momento. Um aplicativo substitui uma imagem padrão usando a [**função SetSystemCursor.**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor) A imagem a seguir mostra vários cursores padrão do Windows Vista:

![cursores padrão, incluindo mão, sinal de quatro setas, seta com ponto de interrogação, círculo, caneta](images/cursorsstandard.png)

Um aplicativo pode usar a [**função GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) para recuperar a imagem atual de um cursor e pode desenhar o cursor usando a [**função DrawIconEx.**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) Para desenhar a imagem padrão para um cursor padrão, especifique o sinalizador **DI \_ COMPAT** na chamada para **DrawIconEx.** Se você não especificar o sinalizador **DI \_ COMPAT,** **DrawIconEx** desenhará o cursor padrão usando a imagem especificada pelo usuário.

Cursores personalizados são projetados para uso em um aplicativo específico e podem ser qualquer design definido pelo desenvolvedor. A ilustração a seguir mostra vários cursores personalizados.

![cursores personalizados, incluindo mão, chocolate, sorvete,watch em mãos, metronome](images/cursorscustom.png)

Os cursores podem ser monocromáticos ou de cor e estáticos ou animados. O tipo de cursor usado em um sistema de computador específico depende da exibição do sistema. Exibições antigas, como VGA, não são suportadas por cor nem cursores animados. Novas exibições, cujos drivers de exibição usam o mecanismo DIB (bitmap independente do dispositivo), são suportadas.

Cursores e ícones são semelhantes e podem ser usados de forma intercambiável em muitas situações. A única diferença entre eles é que uma imagem especificada como um cursor deve estar no formato ao qual a exibição pode dar suporte. Por exemplo, um cursor deve ser monocromático para uma exibição de VGA.

Esta visão geral fornece informações sobre os seguintes tópicos:

-   [O ponto de a quente](#the-hot-spot)
-   [O mouse e o cursor](#the-mouse-and-the-cursor)
-   [Criação de cursor](#cursor-creation)
-   [Localização e aparência do cursor](#cursor-location-and-appearance)
-   [Cursor Desacordo](#cursor-confinement)
-   [Destruição do cursor](#cursor-destruction)
-   [Duplicação do cursor](#cursor-duplication)
-   [O cursor de classe window](#the-window-class-cursor)

## <a name="the-hot-spot"></a>O ponto de a quente

No cursor, um pixel  chamado ponto quente marca o local exato da tela afetado por um evento do mouse, como clicar em um botão do mouse. Normalmente, o ponto quente é o ponto focal do cursor. O sistema rastreia e reconhece esse ponto como a posição do cursor. Por exemplo, os pontos de calor típicos são o pixel na ponta de um cursor em forma de seta e o pixel no meio de um cursor em forma de arco cruzado. As imagens a seguir mostram dois cursores de um programa de desenho, nos quais os pontos de calor estão associados à dica do pincel e à cruz da tinta.

![pontos de calor em dois cursores](images/cursorhotspot.png)

Quando ocorre um evento de entrada do mouse, o driver do mouse converte o evento em uma mensagem apropriada do mouse que inclui as coordenadas do ponto de calor. O sistema envia a mensagem do mouse para a janela que contém o ponto de calor ou para a janela que está capturando a entrada do mouse. Para obter mais informações, consulte [Entrada do mouse.](/windows/desktop/inputdev/mouse-input)

## <a name="the-mouse-and-the-cursor"></a>O mouse e o cursor

O sistema reflete o movimento do mouse movendo o cursor na tela de acordo. À medida que o cursor se move sobre diferentes partes das janelas ou para janelas diferentes, o sistema (ou um aplicativo) altera a aparência do cursor. Por exemplo, quando o cursor cruza um hiperlink, o sistema altera o cursor de uma seta para uma mão.

![cursor padrão que muda para uma mão ao longo de um hiperlink](images/cursorchangingstate.png)

Se o sistema não tiver um mouse, o sistema exibirá e move o cursor somente quando o usuário escolher determinados comandos do sistema, como aqueles usados para tamanho ou movimentação de uma janela. Para fornecer ao usuário um método de exibição e movimentação do cursor quando um mouse não está disponível, um aplicativo pode usar as funções de cursor para simular a movimentação do mouse. Dada essa funcionalidade de simulação, o usuário pode usar as teclas de direção para mover o cursor.

## <a name="cursor-creation"></a>Criação de cursor

Como os cursores padrão são predefinidos, não é necessário crie-os. Para usar um cursor padrão, um aplicativo recupera um alça de cursor usando a [**função LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) ou [**LoadImage.**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) Um *identificador de cursor* é um valor exclusivo do **tipo HCURSOR** que identifica um cursor padrão ou personalizado.

Para criar um cursor personalizado para um aplicativo, normalmente você usa um aplicativo gráfico e inclui o cursor como um recurso no arquivo de definição de recursos do aplicativo. Em tempo de operação, [**chame LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) para recuperar o cursor handle. Os recursos de cursor contêm dados para vários dispositivos de exibição diferentes. A **função LoadCursor** seleciona automaticamente os dados mais apropriados para o dispositivo de exibição atual. Para carregar um cursor diretamente de um . CUR ou . Arquivo ANI, use a [**função LoadCursorFromFile.**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)

Você também pode criar um cursor personalizado em tempo de executar usando a função [**CreateIconIndirect,**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) que cria um cursor com base no conteúdo de uma [**estrutura ICONINFO.**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) A [**função GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) preenche essa estrutura com coordenadas de ponto de contato e informações sobre a máscara e a cor associadas.

Os aplicativos devem implementar cursores personalizados como recursos e usar [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) em vez de criar o cursor em tempo de execução. O uso de recursos de cursor evita a dependência do dispositivo, simplifica a localização e permite que os aplicativos compartilhem designs de cursor.

A [**função CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) permite que um aplicativo crie ícones e cursores com base nos dados do recurso. **CreateIconFromResourceEx** cria um cursor com base em dados de recursos binários de outros arquivos executáveis (.exe) ou DLLs. Ele deve ser precedido por chamadas para a [**função LookupIconIdFromDirectoryEx,**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) bem como várias funções de recurso. **LookupIconIdFromDirectoryEx identifica** os dados de cursor mais apropriados para o dispositivo de exibição atual. Para obter mais informações sobre funções de recurso, consulte [Recursos](resources.md).

## <a name="cursor-location-and-appearance"></a>Localização e aparência do cursor

O sistema exibe automaticamente um cursor para o mouse e atualiza sua posição na tela. Você pode obter as coordenadas de tela atuais do cursor e mover o cursor para qualquer local na tela usando as funções [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) e [**SetCursorPos,**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) respectivamente.

Você também pode recuperar o alça para o cursor atual usando a função [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor) e pode definir o cursor usando a [**função SetCursor.**](/windows/desktop/api/Winuser/nf-winuser-setcursor) Depois de chamar **SetCursor**, a aparência do cursor não muda até que o mouse se mova, o cursor é definido explicitamente como um cursor diferente ou um comando do sistema é executado.

Quando o usuário move o mouse, o sistema redesenha o cursor no novo local. O sistema redesenha automaticamente o design do cursor associado à janela para a qual o cursor está apontando.

Você pode ocultar e repetir o cursor, sem alterar o design do cursor, usando a [**função ShowCursor.**](/windows/desktop/api/Winuser/nf-winuser-showcursor) Essa função usa um contador interno para determinar quando ocultar ou exibir o cursor. Uma tentativa de mostrar o cursor incrementa o contador; uma tentativa de ocultar o cursor diminui o contador. O cursor só será visível se esse contador for maior ou igual a zero.

A [**função GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo) obtém as seguintes informações para o cursor global: se o cursor está oculto ou mostrado, o handle para o cursor e as coordenadas do cursor.

## <a name="cursor-confinement"></a>Cursor Desacordo

Você pode limitar o cursor a uma área retangular na tela usando a [**função ClipCursor.**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) Isso é útil para quando o usuário deve responder a um determinado evento dentro da área restrita do retângulo. Por exemplo, você pode usar **ClipCursor** para limitar o cursor a uma caixa de diálogo modal, impedindo que o usuário interaja com outras janelas até que a caixa de diálogo seja fechada.

A [**função GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) recupera as coordenadas de tela da área retangular à qual o cursor está temporariamente restrito. Quando for necessário limitar o cursor, você também pode usar essa função para salvar as coordenadas da área original na qual o cursor pode se mover. Em seguida, você pode restaurar o cursor para a área original quando o novo rebaixamento não for mais necessário.

## <a name="cursor-destruction"></a>Destruição do cursor

Você pode destruir o cursor e liberar a memória usada pelo cursor chamando a [**função DestroyCursor.**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) No entanto, essa função não tem nenhum efeito em um cursor compartilhado. Um cursor compartilhado é válido desde que o módulo do qual ele foi carregado permaneça na memória. As seguintes funções obtém um cursor compartilhado:

-   [**Loadcursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)
-   [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)
-   [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) (se você usar o **sinalizador LR \_ SHARED)**
-   [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) (se você usar o sinalizador **LR \_ COPYRETURNORG** e *o hImage* for um cursor compartilhado)

Quando você não precisar mais de um cursor criado usando a [**função CreateIconIndirect,**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) você deverá destruir o cursor. A [**função DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) destrói o alça do cursor e libera qualquer memória usada pelo cursor. Use essa função somente em cursores que foram criados com **CreateIconIndirect.**

## <a name="cursor-duplication"></a>Duplicação do cursor

A [**função CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor) copia um alça de cursor. Isso permite que o aplicativo ou o código DLL recupere o alça para um cursor pertencente a outro módulo. Em seguida, se o outro módulo for liberado, o módulo que copiou o cursor ainda poderá usar o design do cursor.

Para obter informações sobre como adicionar, remover ou substituir recursos de cursor em arquivos executáveis, consulte [Recursos](resources.md).

## <a name="the-window-class-cursor"></a>O cursor de classe window

Ao registrar uma classe de janela, usando a [**função RegisterClass,**](/windows/desktop/api/winuser/nf-winuser-registerclassa) você pode atribuir a ela um cursor padrão, conhecido como *cursor de classe*. Depois que o aplicativo registra a classe window, cada janela dessa classe tem o cursor de classe especificado.

Para substituir o cursor de classe, processe [**a mensagem WM \_ SETCURSOR.**](wm-setcursor.md) Você também pode substituir um cursor de classe usando a [**função SetClassLong.**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) Essa função altera as configurações de janela padrão para todas as janelas de uma classe especificada. Para obter mais informações, consulte [Cursor de classe](/windows/desktop/winmsg/about-window-classes).

 

 