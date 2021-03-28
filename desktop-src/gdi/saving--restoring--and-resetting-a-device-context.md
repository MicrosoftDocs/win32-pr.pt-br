---
description: 'As funções a seguir permitem que um aplicativo Salve, restaure e Redefina um contexto de dispositivo: SaveDC, RestoreDC e ResetDC.'
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Salvando, restaurando e redefinindo um contexto de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2714360c07f4a4eca354ede5b460864cc897e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967960"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a>Salvando, restaurando e redefinindo um contexto de dispositivo

As funções a seguir permitem que um aplicativo Salve, restaure e Redefina um contexto de dispositivo: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)e [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca). A função SaveDC registra em uma pilha GDI especial os objetos gráficos atuais do DC e seus atributos e modos gráficos. Um aplicativo de desenho pode chamar essa função antes que um usuário comece a desenhar e salve o estado original do aplicativo fornecendo um Tablet limpo para o usuário. Para retornar a esse estado original, o aplicativo chama a função RestoreDC.

O [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) é fornecido para redefinir os dados do DC da impressora. Um aplicativo chama essa função para redefinir a orientação do papel, o tamanho do papel, o fator de dimensionamento de saída, o número de cópias a serem impressadas, a origem do papel (ou o compartimento), o modo duplex e assim por diante. Normalmente, um aplicativo chama essa função depois que um usuário altera uma das opções de impressora e o sistema emitiu uma mensagem de [**\_ DEVMODECHANGE do WM**](wm-devmodechange.md) .

 

 



