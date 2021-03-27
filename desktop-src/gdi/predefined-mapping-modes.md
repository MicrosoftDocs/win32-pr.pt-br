---
description: Dos seis modos de mapeamento predefinidos, um é dependente de dispositivo ( \_ texto mm) e os cinco restantes (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC e mm \_ TWIPS) são independentes de dispositivo.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Modos de mapeamento predefinidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f252f587e98a739306a84450a1d9669ed21873cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967608"
---
# <a name="predefined-mapping-modes"></a><span data-ttu-id="097c1-103">Modos de mapeamento predefinidos</span><span class="sxs-lookup"><span data-stu-id="097c1-103">Predefined Mapping Modes</span></span>

<span data-ttu-id="097c1-104">Dos seis modos de mapeamento predefinidos, um é dependente de dispositivo ( \_ texto mm) e os cinco restantes (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC e mm \_ TWIPS) são independentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="097c1-104">Of the six predefined mapping modes, one is device dependent (MM\_TEXT) and the remaining five (MM\_HIENGLISH, MM\_LOENGLISH, MM\_HIMETRIC, MM\_LOMETRIC, and MM\_TWIPS) are device independent.</span></span>

<span data-ttu-id="097c1-105">O modo de mapeamento padrão é \_ texto mm.</span><span class="sxs-lookup"><span data-stu-id="097c1-105">The default mapping mode is MM\_TEXT.</span></span> <span data-ttu-id="097c1-106">Uma unidade lógica é igual a um pixel.</span><span class="sxs-lookup"><span data-stu-id="097c1-106">One logical unit equals one pixel.</span></span> <span data-ttu-id="097c1-107">X positivo está à direita e y positivo está inoperante.</span><span class="sxs-lookup"><span data-stu-id="097c1-107">Positive x is to the right, and positive y is down.</span></span> <span data-ttu-id="097c1-108">Esse modo é mapeado diretamente para o sistema de coordenadas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="097c1-108">This mode maps directly to the device's coordinate system.</span></span> <span data-ttu-id="097c1-109">O mapeamento lógico para físico envolve apenas um deslocamento em x e y que é definido pela janela controlada pelo aplicativo e origens do visor.</span><span class="sxs-lookup"><span data-stu-id="097c1-109">The logical-to-physical mapping involves only an offset in x and y that is defined by the application-controlled window and viewport origins.</span></span> <span data-ttu-id="097c1-110">As extensões viewport e Window são todas definidas como 1, criando um mapeamento um-para-um.</span><span class="sxs-lookup"><span data-stu-id="097c1-110">The viewport and window extents are all set to 1, creating a one-to-one mapping.</span></span>

<span data-ttu-id="097c1-111">Os aplicativos que exibem formas geométricas (círculos, quadrados, polígonos e assim por diante) usam um dos modos de mapeamento independentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="097c1-111">Applications that display geometric shapes (circles, squares, polygons, and so on) make use of one of the device-independent mapping modes.</span></span> <span data-ttu-id="097c1-112">Por exemplo, se você estiver escrevendo um aplicativo para fornecer recursos de gráfico para um programa de planilha e desejar garantir que o diâmetro de cada gráfico de pizza seja de 2 polegadas, use o \_ modo de mapeamento LOENGLISH mm e chame as funções apropriadas para desenhar e preencher o gráfico.</span><span class="sxs-lookup"><span data-stu-id="097c1-112">For example, if you are writing an application to provide charting capabilities for a spreadsheet program and want to guarantee that the diameter of each pie chart is 2 inches, use the MM\_LOENGLISH mapping mode and call the appropriate functions to draw and fill the chart.</span></span> <span data-ttu-id="097c1-113">Especificando MM \_ LOENGLISH, garante que o diâmetro do gráfico seja consistente em qualquer exibição ou impressora.</span><span class="sxs-lookup"><span data-stu-id="097c1-113">Specifying MM\_LOENGLISH, guarantees that the diameter of the chart is consistent on any display or printer.</span></span> <span data-ttu-id="097c1-114">Se \_ o texto mm for usado em vez de mm \_ LOENGLISH, um gráfico que parece circular em uma tela VGA apareceria elíptico em uma exibição de EGA e pareceria muito pequeno em uma impressora laser de 300 dpi (pontos por polegada).</span><span class="sxs-lookup"><span data-stu-id="097c1-114">If MM\_TEXT is used instead of MM\_LOENGLISH, a chart that appears circular on a VGA display would appear elliptical on an EGA display and would appear very small on a 300 dpi (dots per inch) laser printer.</span></span>

 

 



