---
description: DDBs (bitmaps dependentes do dispositivo) são descritos usando uma única estrutura, a estrutura BITMAP.
ms.assetid: 63ff9cd6-cd07-4085-b166-268e4d9b7aad
title: Device-Dependent bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3cf365b0f3b11e4a79bb0e7b1e1749d75ca356d41454e40cc6c31f383a74701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887230"
---
# <a name="device-dependent-bitmaps"></a>Device-Dependent bitmaps

DDBs (bitmaps dependentes do dispositivo) são descritos usando uma única estrutura, a [**estrutura BITMAP.**](/windows/win32/api/wingdi/ns-wingdi-bitmap) Os membros dessa estrutura especificam a largura e a altura de uma região retangular, em pixels; a largura da matriz que mapeia entradas da paleta de dispositivos para pixels; e o formato de cor do dispositivo, em termos de planos de cores e bits por pixel. Um aplicativo pode recuperar o formato de cor de um dispositivo chamando a [**função GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) e especificando as constantes apropriadas. Observe que um DDB não contém valores de cor; em vez disso, as cores estão em um formato dependente do dispositivo. Para obter mais informações, consulte [Color in Bitmaps](color-in-bitmaps.md). Como cada dispositivo pode ter seu próprio conjunto de cores, um DDB criado para um dispositivo pode não ser exibido bem em um dispositivo diferente.

Para usar um DDB em um contexto de dispositivo, ele deve ter a organização de cores desse contexto de dispositivo. Portanto, um DDB geralmente é chamado de *bitmap* compatível e geralmente tem um desempenho de GDI melhor do que um DIB. Por exemplo, para criar um bitmap para memória de vídeo, é melhor usar um bitmap compatível com o mesmo formato de cor que a exibição primária. Uma vez na memória de vídeo, renderizar para o bitmap e exibi-lo na tela é significativamente mais rápido do que de uma superfície de memória do sistema ou diretamente de um DIB.

Além de permitir um melhor desempenho de GDI, os bitmaps compatíveis são usados para capturar imagens (consulte Capturando uma imagem [)](capturing-an-image.md) e para criar bitmaps em tempo de execução para menus, consulte "Criando o bitmap" em (consulte [Usando menus](../menurc/using-menus.md) ).

Para transferir um bitmap entre dispositivos com organização de cores diferentes, use [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) para converter o bitmap compatível em um DIB e chame [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) ou [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) para exibir o DIB para o segundo dispositivo.

Há dois tipos de DDBs: descartável e não acessível. Um DDB descartável é um bitmap que o sistema descartará se o bitmap não estiver selecionado em um DC e se a memória do sistema estiver baixa. A [**função CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) cria bitmaps que podem ser descartados. As [**funções CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap)e [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) criam bitmaps nãocardáveis.

Um aplicativo pode criar um DDB de um DIB inicializando as estruturas necessárias e chamando a [**função CreateDIBitmap.**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) Especificar CBM INIT na chamada para CreateDIBitmap é equivalente a chamar a função \_ [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) para criar um DDB no formato do dispositivo e, em seguida, chamar a [**função SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) para converter os bits DIB para o DDB.  Para determinar se um dispositivo dá suporte à **função SetDIBits,** chame a função [**GetDeviceCaps,**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) especificando RC DI BITMAP como o \_ sinalizador \_ RASTERCAPS.

 

 
