---
description: Os bitmaps dependentes do dispositivo (DDBs) são descritos usando uma única estrutura, a estrutura de BITMAP.
ms.assetid: 63ff9cd6-cd07-4085-b166-268e4d9b7aad
title: Device-Dependent bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a3de2c59509c71b38f9981df330b3b28effa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091195"
---
# <a name="device-dependent-bitmaps"></a>Device-Dependent bitmaps

Os bitmaps dependentes do dispositivo (DDBs) são descritos usando uma única estrutura, a estrutura de [**bitmap**](/windows/win32/api/wingdi/ns-wingdi-bitmap) . Os membros dessa estrutura especificam a largura e a altura de uma região retangular, em pixels; a largura da matriz que mapeia as entradas da paleta do dispositivo para pixels; e o formato de cor do dispositivo, em termos de planos de cores e bits por pixel. Um aplicativo pode recuperar o formato de cor de um dispositivo chamando a função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) e especificando as constantes apropriadas. Observe que um BDD não contém valores de cor; em vez disso, as cores estão em um formato dependente de dispositivo. Para obter mais informações, consulte [cor em bitmaps](color-in-bitmaps.md). Como cada dispositivo pode ter seu próprio conjunto de cores, um BDD criado para um dispositivo pode não ser exibido bem em um dispositivo diferente.

Para usar um BDD em um contexto de dispositivo, ele deve ter a organização de cores desse contexto de dispositivo. Assim, um BDD é geralmente chamado de *bitmap compatível* e geralmente tem melhor desempenho de GDI do que um DIB. Por exemplo, para criar um bitmap para a memória de vídeo, é melhor usar um bitmap compatível com o mesmo formato de cor que a exibição primária. Uma vez na memória de vídeo, renderizar para o bitmap e exibi-lo para a tela é significativamente mais rápido do que a partir de uma superfície de memória do sistema ou diretamente de um DIB.

Além de permitir melhor desempenho de GDI, bitmaps compatíveis são usados para capturar imagens (consulte [captura de uma imagem](capturing-an-image.md) ) e para criar bitmaps em tempo de execução para menus, consulte "criando o bitmap" em (consulte [usando menus](../menurc/using-menus.md) ).

Para transferir um bitmap entre dispositivos com uma organização de cores diferente, use [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) para converter o bitmap compatível em DIB e chamar [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) ou [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) para exibir o DIB para o segundo dispositivo.

Há dois tipos de DDBs: descartável e não descartável. Um BDD Descartado é um bitmap que o sistema descarta se o bitmap não estiver selecionado em um controlador de domínio e se a memória do sistema estiver baixa. A função [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) cria bitmaps descartados. As funções [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap)e [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) criam bitmaps não descartáveis.

Um aplicativo pode criar um BDD de um DIB Inicializando as estruturas necessárias e chamando a função [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) . Especificar CBM \_ init na chamada para **CreateDIBitmap** é equivalente a chamar a função [**CREATECOMPATIBLEBITMAP**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) para criar um BDD no formato do dispositivo e, em seguida, chamar a função [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) para converter os bits DIB no BDD. Para determinar se um dispositivo dá suporte à função **SetDIBits** , chame a função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) , especificando \_ o \_ bitmap de di RC como o sinalizador RasterCaps.

 

 
