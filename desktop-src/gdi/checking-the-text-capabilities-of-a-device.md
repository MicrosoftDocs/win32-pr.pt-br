---
description: Você pode usar as funções EnumFonts e EnumFontFamilies para enumerar as fontes que estão disponíveis em um contexto de dispositivo de memória compatível com a impressora.
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: Verificando os recursos de texto de um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd1a4ddc0c678c775c6c068216e60ead234d757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988838"
---
# <a name="checking-the-text-capabilities-of-a-device"></a><span data-ttu-id="2608f-103">Verificando os recursos de texto de um dispositivo</span><span class="sxs-lookup"><span data-stu-id="2608f-103">Checking the Text Capabilities of a Device</span></span>

<span data-ttu-id="2608f-104">Você pode usar as funções [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) e [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) para enumerar as fontes que estão disponíveis em um contexto de dispositivo de memória compatível com a impressora.</span><span class="sxs-lookup"><span data-stu-id="2608f-104">You can use the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions to enumerate the fonts that are available in a printer-compatible memory device context.</span></span> <span data-ttu-id="2608f-105">Você também pode usar a função [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) para recuperar informações sobre os recursos de texto de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2608f-105">You can also use the [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve information about the text capabilities of a device.</span></span> <span data-ttu-id="2608f-106">Chamando a função [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) com o índice NUMFONTS, você pode determinar o número mínimo de fontes com suporte em uma impressora.</span><span class="sxs-lookup"><span data-stu-id="2608f-106">By calling the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function with the NUMFONTS index, you can determine the minimum number of fonts supported by a printer.</span></span> <span data-ttu-id="2608f-107">(Uma impressora individual pode dar suporte a mais fontes do que o especificado no valor de retorno de **GetDeviceCaps** com o índice NUMFONTS.) Usando o índice textcaps, você pode identificar muitos dos recursos de texto do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="2608f-107">(An individual printer may support more fonts than specified in the return value from **GetDeviceCaps** with the NUMFONTS index.) By using the TEXTCAPS index, you can identify many of the text capabilities of the specified device.</span></span>

 

 
