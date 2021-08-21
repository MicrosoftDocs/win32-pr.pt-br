---
description: Dos seis modos de mapeamento predefinidos, um é dependente de dispositivo ( \_ texto mm) e os cinco restantes (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC e mm \_ TWIPS) são independentes de dispositivo.
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

Dos seis modos de mapeamento predefinidos, um é dependente de dispositivo ( \_ texto mm) e os cinco restantes (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC e mm \_ TWIPS) são independentes de dispositivo.

O modo de mapeamento padrão é \_ texto mm. Uma unidade lógica é igual a um pixel. X positivo está à direita e y positivo está inoperante. Esse modo é mapeado diretamente para o sistema de coordenadas do dispositivo. O mapeamento lógico para físico envolve apenas um deslocamento em x e y que é definido pela janela controlada pelo aplicativo e origens do visor. As extensões viewport e Window são todas definidas como 1, criando um mapeamento um-para-um.

Os aplicativos que exibem formas geométricas (círculos, quadrados, polígonos e assim por diante) usam um dos modos de mapeamento independentes de dispositivo. Por exemplo, se você estiver escrevendo um aplicativo para fornecer recursos de gráfico para um programa de planilha e desejar garantir que o diâmetro de cada gráfico de pizza seja de 2 polegadas, use o \_ modo de mapeamento LOENGLISH mm e chame as funções apropriadas para desenhar e preencher o gráfico. Especificando MM \_ LOENGLISH, garante que o diâmetro do gráfico seja consistente em qualquer exibição ou impressora. Se \_ o texto mm for usado em vez de mm \_ LOENGLISH, um gráfico que parece circular em uma tela VGA apareceria elíptico em uma exibição de EGA e pareceria muito pequeno em uma impressora laser de 300 dpi (pontos por polegada).

 

 



