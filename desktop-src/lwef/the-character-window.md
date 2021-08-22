---
title: A janela de caracteres
description: A janela de caracteres
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426aab4cbd6e0ad536135cb47ec9a636ea56a0509f3fb0cb75ad6440addc62da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474882"
---
# <a name="the-character-window"></a>A janela de caracteres

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O Microsoft Agent exibe caracteres animados em suas próprias janelas que sempre aparecem na parte superior da janela ordem z (ou seja, sempre na parte superior). Um usuário pode mover a janela de um caractere arrastando o caractere com o botão esquerdo do mouse. A imagem de caractere se move com o ponteiro . Além disso, um aplicativo pode mover um caractere usando o [**método MoveTo.**](moveto-method.md)

Quando o usuário clica com o botão direito do mouse em um caractere, é exibido um menu pop-up que exibe os seguintes comandos:

Abrir \| a janela Fechar <span class="underline">Comandos</span>do Oice V

<span class="underline">H</span>ide

----------------------------…

Comando\*


*OtherHostingApplicationCaption\*\**

\*Os comandos listados são baseados no cliente input-active. Para obter mais informações sobre como definir comandos que aparecem no menu pop-up, consulte Visão geral da Interface de Programação do Microsoft Agent.

\*\*As entradas listadas são todos os outros aplicativos que hospedam o caractere no momento. Para obter mais informações sobre como definir essa entrada, consulte Visão geral da Interface de Programação do Microsoft Agent.

O comando \| Abrir Janela De Comandos de Voz Aberta controla a exibição da Janela Comandos do caractere ativo atual. Se os serviços de reconhecimento de fala estão desabilitados, esse comando é desabilitado. Se os serviços de reconhecimento de fala não estão instalados, esse comando não é exibido.

O comando Ocultar oculta o caractere. A animação atribuída ao  estado Ocultando do caractere é reproduz e oculta o caractere. A letra "H" em ocultar é a chave de acesso do comando (mnemônico).

Os comandos para os aplicativos que hospedam atualmente o caractere seguem o comando Ocultar, precedido por um separador. Em seguida, os nomes de outros aplicativos que usam o caractere são exibidos, também precedido por um separador.

 

 




