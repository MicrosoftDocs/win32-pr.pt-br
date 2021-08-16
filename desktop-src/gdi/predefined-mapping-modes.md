---
description: Dos seis modos de mapeamento predefinidos, um depende do dispositivo (MM TEXT) e os cinco restantes \_ (MM \_ HIENGLISH, MM \_ LOENGLISH, MM \_ HIMETRIC, MM LOMETRIC e \_ MM \_ TWIPS) são independentes de dispositivo.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Modos de mapeamento predefinidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c0eecce6196672db11d61326c82364c1fde1d1b494e48ff77e214e79df91e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037674"
---
# <a name="predefined-mapping-modes"></a>Modos de mapeamento predefinidos

Dos seis modos de mapeamento predefinidos, um depende do dispositivo (MM TEXT) e os cinco restantes \_ (MM \_ HIENGLISH, MM \_ LOENGLISH, MM \_ HIMETRIC, MM LOMETRIC e \_ MM \_ TWIPS) são independentes de dispositivo.

O modo de mapeamento padrão é MM \_ TEXT. Uma unidade lógica é igual a um pixel. Positivo x está à direita e y positivo está ino mesmo. Esse modo é mapeado diretamente para o sistema de coordenadas do dispositivo. O mapeamento lógico para físico envolve apenas um deslocamento em x e y definido pela janela controlada pelo aplicativo e pelas origens do viewport. O viewport e as extensão de janela são definidos como 1, criando um mapeamento um-para-um.

Aplicativos que exibem formas geométricas (círculos, quadrados, polígonos e assim por diante) usam um dos modos de mapeamento independentes do dispositivo. Por exemplo, se você estiver escrevendo um aplicativo para fornecer recursos de gráfico para um programa de planilha e quiser garantir que o diâmetro de cada gráfico de pizza seja de 2 polegadas, use o modo de mapeamento MM LOENGLISH e chame as funções apropriadas para desenhar e preencher o \_ gráfico. Especificar MM \_ LOENGLISH garante que o diâmetro do gráfico seja consistente em qualquer exibição ou impressora. Se MM TEXT for usado em vez de MM LOENGLISH, um gráfico que aparece circular em uma exibição de VGA aparecerá elíptico em uma exibição EGA e aparecerá muito pequeno em uma impressora \_ \_ de 300 dpi (pontos por polegada).

 

 



