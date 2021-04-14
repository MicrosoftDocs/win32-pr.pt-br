---
title: A janela de caracteres
description: A janela de caracteres
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a386dc769e2b5fe7313b768d1b2debfe4a1131
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104368963"
---
# <a name="the-character-window"></a>A janela de caracteres

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O Microsoft Agent exibe caracteres animados em suas próprias janelas que sempre aparecem na parte superior da ordem z da janela (ou seja, always on Top). Um usuário pode mover a janela de um caractere arrastando o caractere com o botão esquerdo do mouse. A imagem de caractere é movida com o ponteiro. Além disso, um aplicativo pode mover um caractere usando o método [**MoveTo**](moveto-method.md) .

Quando o usuário clica com o botão direito do mouse em um caractere, é exibido um menu pop-up que exibe os seguintes comandos:

Abrir \| fechar a janela de comandos do <span class="underline">V</span>Assis

IDE <span class="underline">H</span>

----------------------------…

Linha\*


*OtherHostingApplicationCaption\*\**

\*Os comandos listados são baseados no cliente de entrada-ativo. Para obter mais informações sobre como definir comandos que aparecem no menu pop-up, consulte Visão geral da interface de programação do Microsoft Agent.

\*\*As entradas listadas são todos os outros aplicativos que estão hospedando o caractere no momento. Para obter mais informações sobre como definir essa entrada, consulte a visão geral da interface de programação do Microsoft Agent.

O \| comando abrir fechar voz comandos da janela controla a exibição da janela comandos do caractere ativo atual. Se os serviços de reconhecimento de fala estiverem desabilitados, esse comando será desabilitado. Se os serviços de reconhecimento de fala não estiverem instalados, esse comando não será exibido.

O comando Hide oculta o caractere. A animação atribuída ao estado de **ocultação** do caractere é reproduzida e oculta o caractere. A letra "H" em Hide é a chave de acesso do comando (mnemônico).

Os comandos para os aplicativos que atualmente hospedam o caractere seguem o comando Hide, precedido por um separador. Em seguida, os nomes de outros aplicativos que usam o caractere são exibidos, também precedidos por um separador.

 

 




