---
description: Um contexto de dispositivo pai permite que um aplicativo minimize o tempo necessário para configurar a região de recorte para uma janela.
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: Os contextos do dispositivo de exibição pai
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e423ceaa65790df35fa55c8dda597cb1bb45019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967623"
---
# <a name="parent-display-device-contexts"></a>Os contextos do dispositivo de exibição pai

Um *contexto de dispositivo pai* permite que um aplicativo minimize o tempo necessário para configurar a região de recorte para uma janela. Um aplicativo normalmente usa contextos de dispositivo pai para acelerar o desenho de janelas de controle sem a necessidade de um contexto de dispositivo privado ou de classe. Por exemplo, o sistema usa contextos de dispositivo pai para botão de ação e controles de edição. Os contextos de dispositivo pai destinam-se ao uso somente com janelas filhas, nunca com janelas de nível superior ou pop-up.

Um aplicativo pode especificar o \_ estilo cs PARENTDC para definir a região de recorte da janela filho para a da janela pai, de forma que o filho possa desenhar no pai. A especificação do CS \_ PARENTDC aprimora o desempenho de um aplicativo porque o sistema não precisa continuar recalculando a região visível para cada janela filho.

Os valores de atributo definidos pela janela pai não são preservados para a janela filho; por exemplo, a janela pai não pode definir o pincel para suas janelas filhas. A única propriedade preservada é a região de recorte. A janela deve cortar sua própria saída nos limites da janela. Como a região de recorte para o contexto do dispositivo pai é idêntica à janela pai, a janela filho pode potencialmente desenhar sobre toda a janela pai, mas o contexto do dispositivo pai não deve ser usado dessa maneira.

O sistema ignorará o \_ estilo cs PARENTDC se a janela pai usar um contexto de dispositivo privado ou de classe, se a janela pai cortar suas janelas filhas ou se a janela filho cortar suas janelas filhas ou irmãs.

 

 



