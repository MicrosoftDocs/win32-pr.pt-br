---
description: Um DC (contexto de dispositivo) é uma estrutura de dados que define os objetos gráficos, seus atributos associados e os modos gráficos que afetam a saída em um dispositivo. Para criar um controlador de domínio, chame a função CreateDC; para recuperar um controlador de domínio, chame a função GetDC.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Bitmaps, contextos de dispositivo e superfícies de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed42215dc98ce179f9d36ddc0a24244c018c4177287d1fdfff974a2814e14d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966386"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a>Bitmaps, contextos de dispositivo e superfícies de desenho

Um DC ( *contexto de dispositivo* ) é uma estrutura de dados que define os objetos gráficos, seus atributos associados e os modos gráficos que afetam a saída em um dispositivo. Para criar um controlador de domínio, chame a função [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) ; para recuperar um controlador de domínio, chame a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .

Antes de retornar um identificador que identifica esse DC, o sistema seleciona uma superfície de desenho no controlador de domínio. Se o aplicativo chamou a função [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) para criar um contexto de dispositivo para uma exibição VGA, as dimensões dessa superfície de desenho serão de 640 a 480 pixels. Se o aplicativo tiver chamado a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) , as dimensões refletirão o tamanho da área do cliente.

Antes que um aplicativo possa começar a desenhar, ele deve selecionar um bitmap com a largura e a altura apropriadas no controlador de domínio chamando a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Quando um aplicativo passa o identificador para o controlador de domínio para uma das funções de desenho da interface de dispositivo de gráficos (GDI), a saída solicitada aparece na superfície de desenho selecionada no controlador de domínio.

Para obter mais informações, consulte [contextos de dispositivo de memória](memory-device-contexts.md).

 

 



