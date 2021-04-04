---
title: Sobre cursores
description: Este tópico discute os cursores padrão.
ms.assetid: 0ca8e51c-1159-47e9-ba3f-5ced0667cadb
keywords:
- recursos, cursores
- cursores, sobre
- cursores, padrão
- cursores padrão
- Função SetSystemCursor
- cursores, personalizado
- cursores personalizados
- cursores, pontos de acesso
- cursores, criando
- Criando cursores
- cursores, local
- cursores, aparência
- destruindo cursores
- duplicando cursores
- cursor de classe
- confinando cursores
- cursores, destruindo
- cursores, duplicando
- cursores, classe
- cursores, confinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d0b91ba4670d2510413240efd742b2e0ba69b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007503"
---
# <a name="about-cursors"></a>Sobre cursores

O Windows fornece um conjunto de cursores padrão que estão disponíveis para qualquer aplicativo a ser usado a qualquer momento. Os arquivos de cabeçalho do SDK contêm identificadores para os cursores padrão — os identificadores começam com o prefixo **IDC \_** .

Cada cursor padrão tem uma imagem padrão correspondente associada. O usuário ou um aplicativo pode substituir a imagem padrão associada a qualquer cursor padrão a qualquer momento. Um aplicativo substitui uma imagem padrão usando a função [**SetSystemCursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor) . A imagem a seguir mostra vários cursores padrão do Windows Vista:

![cursores padrão, incluindo mão, sinal de adição de quatro setas, seta com ponto de interrogação, círculo, caneta](images/cursorsstandard.png)

Um aplicativo pode usar a função [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) para recuperar a imagem atual para um cursor e pode desenhar o cursor usando a função [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) . Para desenhar a imagem padrão para um cursor padrão, especifique o sinalizador de **\_ compatibilidade de di** na chamada para **DrawIconEx**. Se você não especificar o sinalizador **\_ compatível com di** , **DrawIconEx** desenhará o cursor padrão usando a imagem especificada pelo usuário.

Cursores personalizados são projetados para uso em um aplicativo específico e podem ser qualquer design definido pelo desenvolvedor. A ilustração a seguir mostra vários cursores personalizados.

![cursores personalizados, incluindo mão, banana, tambor, pulso disponível, Metronome](images/cursorscustom.png)

Os cursores podem ser monocromáticos ou coloridos, tanto estáticos quanto animados. O tipo de cursor usado em um sistema de computador específico depende da tela do sistema. Vídeos antigos, como VGA, não dão suporte a cores ou cursores animados. Novos vídeos, cujos drivers de exibição usam o mecanismo DIB (bitmap independente de dispositivo), dão suporte a eles.

Cursores e ícones são semelhantes e podem ser usados de maneira intercambiável em muitas situações. A única diferença entre eles é que uma imagem especificada como um cursor deve estar no formato ao qual a exibição pode dar suporte. Por exemplo, um cursor deve ser monocromático para uma tela VGA.

Esta visão geral fornece informações sobre os seguintes tópicos:

-   [O ponto de acesso](#the-hot-spot)
-   [O mouse e o cursor](#the-mouse-and-the-cursor)
-   [Criação de cursor](#cursor-creation)
-   [Localização e aparência do cursor](#cursor-location-and-appearance)
-   [Confinamento do cursor](#cursor-confinement)
-   [Destruição de cursor](#cursor-destruction)
-   [Duplicação do cursor](#cursor-duplication)
-   [O cursor de classe de janela](#the-window-class-cursor)

## <a name="the-hot-spot"></a>O ponto de acesso

No cursor, um pixel chamado ponto de *acesso* marca a localização exata da tela que é afetada por um evento do mouse, como clicar em um botão do mouse. Normalmente, o ponto de acesso é o foco do cursor. O sistema rastreia e reconhece esse ponto como a posição do cursor. Por exemplo, pontos de acesso típicos são o pixel na ponta de um cursor em forma de seta e o pixel no meio de um cursor em forma de cruz. As imagens a seguir mostram dois cursores de um programa de desenho, nos quais os pontos de acesso estão associados à ponta do pincel e a Cruz da pintura pode.

![pontos de acesso em dois cursores](images/cursorhotspot.png)

Quando ocorre um evento de entrada do mouse, o driver do mouse converte o evento em uma mensagem de mouse apropriada que inclui as coordenadas do ponto de acesso. O sistema envia a mensagem do mouse para a janela que contém o ponto de acesso ou para a janela que está capturando a entrada do mouse. Para obter mais informações, consulte [entrada do mouse](/windows/desktop/inputdev/mouse-input).

## <a name="the-mouse-and-the-cursor"></a>O mouse e o cursor

O sistema reflete a movimentação do mouse movendo o cursor na tela de acordo. À medida que o cursor se move sobre diferentes partes do Windows ou para janelas diferentes, o sistema (ou um aplicativo) altera a aparência do cursor. Por exemplo, quando o cursor cruza um hiperlink, o sistema altera o cursor de uma seta para uma mão.

![cursor padrão mudando para uma mão quando sobre um hiperlink](images/cursorchangingstate.png)

Se o sistema não tiver um mouse, o sistema exibirá e moverá o cursor somente quando o usuário escolher determinados comandos do sistema, como aqueles usados para dimensionar ou mover uma janela. Para fornecer ao usuário um método de exibir e mover o cursor quando um mouse não está disponível, um aplicativo pode usar as funções de cursor para simular o movimento do mouse. Dada esse recurso de simulação, o usuário pode usar as teclas de direção para mover o cursor.

## <a name="cursor-creation"></a>Criação de cursor

Como os cursores padrão são predefinidos, não é necessário criá-los. Para usar um cursor padrão, um aplicativo recupera um identificador de cursor usando a função [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) . Um *identificador de cursor* é um valor exclusivo do tipo **hCursor** que identifica um cursor padrão ou personalizado.

Para criar um cursor personalizado para um aplicativo, você normalmente usa um aplicativo gráfico e inclui o cursor como um recurso no arquivo de definição de recurso do aplicativo. Em tempo de execução, chame [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) para recuperar a alça do cursor. Os recursos do cursor contêm dados para vários dispositivos de vídeo diferentes. A função **LoadCursor** seleciona automaticamente os dados mais apropriados para o dispositivo de vídeo atual. Para carregar um cursor diretamente de um. CUR ou. Arquivo ANI, use a função [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea) .

Você também pode criar um cursor personalizado em tempo de execução usando a função [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , que cria um cursor com base no conteúdo de uma estrutura [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) . A função [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) preenche essa estrutura com coordenadas de pontos de acesso e informações relacionadas à máscara e à cor associadas.

Os aplicativos devem implementar cursores personalizados como recursos e usar [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) em vez de criar o cursor em tempo de execução. O uso de recursos de cursor evita a dependência do dispositivo, simplifica a localização e permite que os aplicativos compartilhem designs de cursor.

A função [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) permite que um aplicativo crie ícones e cursores com base nos dados do recurso. **CreateIconFromResourceEx** cria um cursor baseado em dados de recursos binários de outros arquivos ou DLLs executáveis (. exe). Ele deve ser precedido por chamadas para a função [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) , bem como várias funções de recurso. **LookupIconIdFromDirectoryEx** identifica os dados de cursor mais apropriados para o dispositivo de vídeo atual. Para obter mais informações sobre funções de recurso, consulte [recursos](resources.md).

## <a name="cursor-location-and-appearance"></a>Localização e aparência do cursor

O sistema exibe automaticamente um cursor para o mouse e atualiza sua posição na tela. Você pode obter as coordenadas da tela atual do cursor e mover o cursor para qualquer local na tela usando as funções [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) e [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) , respectivamente.

Você também pode recuperar o identificador para o cursor atual usando a função [**getCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor) e pode definir o cursor usando a função [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) . Depois de chamar **SetCursor**, a aparência do cursor não é alterada até que o mouse se mova, o cursor é explicitamente definido como um cursor diferente ou um comando do sistema é executado.

Quando o usuário move o mouse, o sistema redesenha o cursor no novo local. O sistema redesenha automaticamente o design do cursor associado à janela à qual o cursor está apontando.

Você pode ocultar e reexibir o cursor, sem alterar o design do cursor, usando a função de apresentação do [**cursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor) . Essa função usa um contador interno para determinar quando ocultar ou exibir o cursor. Uma tentativa de mostrar o cursor incrementa o contador; uma tentativa de ocultar o cursor diminui o contador. O cursor ficará visível somente se esse contador for maior ou igual a zero.

A função [**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo) Obtém as seguintes informações para o cursor global: se o cursor está oculto ou mostrado, o identificador para o cursor e as coordenadas do cursor.

## <a name="cursor-confinement"></a>Confinamento do cursor

Você pode restringir o cursor a uma área retangular na tela usando a função [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) . Isso é útil quando o usuário deve responder a um determinado evento dentro da área confinada do retângulo. Por exemplo, você pode usar **ClipCursor** para restringir o cursor a uma caixa de diálogo modal, impedindo que o usuário interaja com outras janelas até que a caixa de diálogo seja fechada.

A função [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) recupera as coordenadas de tela da área retangular para a qual o cursor está temporariamente confinado. Quando for necessário restringir o cursor, você também poderá usar essa função para salvar as coordenadas da área original na qual o cursor pode ser movido. Em seguida, você pode restaurar o cursor para a área original quando o novo confinamento não for mais necessário.

## <a name="cursor-destruction"></a>Destruição de cursor

Você pode destruir a alça do cursor e liberar a memória do cursor usado chamando a função [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) . No entanto, essa função não tem nenhum efeito em um cursor compartilhado. Um cursor compartilhado é válido contanto que o módulo do qual ele foi carregado permaneça na memória. As seguintes funções obtêm um cursor compartilhado:

-   [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)
-   [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)
-   [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) (se você usar o **sinalizador \_ compartilhado do LR** )
-   [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) (se você usar o sinalizador **LR \_ COPYRETURNORG** e o *hImage* for um cursor compartilhado)

Quando você não precisar mais de um cursor criado usando a função [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , deverá destruir o cursor. A função [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) destrói a alça do cursor e libera qualquer memória usada pelo cursor. Use essa função somente em cursores que foram criados com **CreateIconIndirect**.

## <a name="cursor-duplication"></a>Duplicação do cursor

A função [**CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor) copia um identificador de cursor. Isso permite que o código de aplicativo ou DLL recupere o identificador para um cursor de propriedade de outro módulo. Em seguida, se o outro módulo for liberado, o módulo que copiou o cursor ainda poderá usar o design do cursor.

Para obter informações sobre como adicionar, remover ou substituir recursos de cursor em arquivos executáveis, consulte [recursos](resources.md).

## <a name="the-window-class-cursor"></a>O cursor de classe de janela

Ao registrar uma classe de janela, usando a função [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) , você pode atribuir a ela um cursor padrão, conhecido como *cursor de classe*. Depois que o aplicativo registra a classe Window, cada janela dessa classe tem o cursor de classe especificado.

Para substituir o cursor de classe, processe a mensagem de [**\_ SetCursor do WM**](wm-setcursor.md) . Você também pode substituir um cursor de classe usando a função [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) . Essa função altera as configurações de janela padrão para todas as janelas de uma classe especificada. Para obter mais informações, consulte [cursor de classe](/windows/desktop/winmsg/about-window-classes).

 

 