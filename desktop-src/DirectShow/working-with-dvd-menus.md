---
description: Trabalhando com menus de DVD
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Trabalhando com menus de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758044"
---
# <a name="working-with-dvd-menus"></a>Trabalhando com menus de DVD

O navegador de DVD pode mostrar um menu quando o usuário ativa um botão ou quando o navegador entra no primeiro domínio de reprodução. Para mostrar um menu programaticamente, chame o método [**IDvdControl2:: domenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) .

Há várias maneiras de selecionar botões de menu programaticamente:

-   Para selecionar um botão por número, chame [**IDvdControl2:: SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton). Os botões são numerados de 1 a 36. O método [**IDvdInfo2:: GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) retorna o número de botões disponíveis.
-   Para selecionar um botão relativo à posição do botão atualmente selecionado, chame [**IDvdControl2:: SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton). Você pode selecionar um botão na direção para cima, para baixo, para a esquerda ou para a direita.
-   Para selecionar um botão por suas coordenadas dentro da janela, chame [**IDvdControl2:: SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition). Esse método usa coordenadas (x, y) em relação à área do cliente da janela de vídeo. (Para o modo sem janela, essa é a janela do aplicativo.) Se não houver nenhum botão nesse local, o método retornará VFW \_ E \_ \_ nenhum botão de DVD \_ .

Além disso, há várias maneiras de ativar um botão:

-   Para ativar um botão por número, chame [**IDvdControl2:: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).
-   Para ativar um botão por suas coordenadas, chame [**IDvdControl2:: ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).
-   Para ativar o botão que está selecionado no momento, chame [**IDvdControl2:: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton). Se nenhum botão for selecionado, o método retornará VFW \_ E \_ \_ nenhum botão de DVD \_ .

Tenha em mente que a seleção de um botão simplesmente realça suas bordas. Para fazer com que o comando associado seja acionado, o botão deve ser ativado. A ativação de um botão programaticamente pode ser feita de várias maneiras, mas o botão sempre deve ser selecionado para que possa ser ativado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



