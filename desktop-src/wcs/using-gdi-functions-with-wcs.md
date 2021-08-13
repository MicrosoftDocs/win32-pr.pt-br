---
title: Uso de funções GDI com WCS
description: Há várias funções na interface gráfica de dispositivo (GDI) que usam ou operam em dados de cores.
ms.assetid: a19ec8b9-11c9-4fde-a99a-7f4a112b49e7
keywords:
- Windows Sistema de cores (WCS), interface gráfica de dispositivo (GDI)
- WCS (Windows sistema de cores), GDI (graphics device interface)
- gerenciamento de cores de imagem, interface gráfica de dispositivo (GDI)
- gerenciamento de cores, interface gráfica de dispositivo (GDI)
- cores, interface gráfica de dispositivo (GDI)
- interface gráfica do dispositivo (GDI)
- GDI (interface de dispositivo de gráficos)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a104378ae46e6b9519d6f795d280d45c28c8fa3fdc7d1e34aae609bcdbd195d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118444673"
---
# <a name="using-gdi-functions-with-wcs"></a>Uso de funções GDI com WCS

Há várias funções na interface gráfica de dispositivo (GDI) que usam ou operam em dados de cores. Alguns estão habilitados para uso com o WCS e outros não. As seguintes funções GDI são relevantes para ICM:

-   [Funções de contexto de dispositivo com WCS](#device-context-functions-with-wcs)
-   [Funções de caneta e pincel com o WCS](#pen-and-brush-functions-with-wcs)
-   [Funções de saída de texto com WCS](#text-output-functions-with-wcs)
-   [Funções de bitmap com WCS](#bitmap-functions-with-wcs)

## <a name="device-context-functions-with-wcs"></a>Funções de contexto de dispositivo com WCS



|    Função                |   Descrição                                                                                                                                                                                                                              |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CreateCompatibleDC | se o contexto do dispositivo (DC) que é passado para essa função por meio de seu parâmetro hdc estiver habilitado para ICM, o DC que a função cria também será habilitado ICM. Os espaços de cores de origem e de destino são especificados no controlador de domínio. |
| CreateDC           | ICM pode ser habilitado definindo o membro dmICMMethod da estrutura DEVMODE apontada pelo parâmetro pInitData para o valor apropriado. Para obter detalhes, consulte a documentação no SDK da plataforma na estrutura DEVMODE.  |
| ResetDC            | O perfil de cor do contexto do dispositivo especificado pelo parâmetro HDC será redefinido com base nas informações na estrutura DEVMODE especificada pelo parâmetro lpInitData.                                                   |



 

## <a name="pen-and-brush-functions-with-wcs"></a>Funções de caneta e pincel com o WCS



|    Função                |   Descrição                                                                                                                                                                                                                              |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Funções de pincel | Nenhum gerenciamento de cores é feito na criação do pincel. no entanto, o gerenciamento de cores será executado quando o pincel for selecionado em um DC habilitado para ICM. |
| CreatePen       | Nenhum gerenciamento de cores é feito na criação da caneta. no entanto, o gerenciamento de cores será executado quando o pincel for selecionado em um DC habilitado para ICM.   |
| ExtCreatePen    | Nenhum gerenciamento de cores é feito na criação da caneta. no entanto, o gerenciamento de cores será executado quando o pincel for selecionado em um DC habilitado para ICM.   |
| SelectObject    | Se o objeto que está sendo selecionado for um pincel ou uma caneta, o gerenciamento de cores será executado.                                                              |
| SetDCBrushColor | O gerenciamento de cores será executado se o WCS estiver habilitado.                                                                                              |
| SetDCPenColor   | O gerenciamento de cores será executado se o WCS estiver habilitado.                                                                                              |



 

## <a name="text-output-functions-with-wcs"></a>Funções de saída de texto com WCS



|    Função                |   Descrição                                                                                                                                                                                                                              |
|--------------|--------------------------------------------------|
| SetBkColor   | O gerenciamento de cores será executado se o WCS estiver habilitado. |
| SetTextColor | O gerenciamento de cores será executado se o WCS estiver habilitado. |



 

## <a name="bitmap-functions-with-wcs"></a>Funções de bitmap com WCS



|    Função                |   Descrição                                                                                                                                                                                                                              |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BitBlt            | Nenhum gerenciamento de cores é executado quando blits ocorre.                                                                                                                                                                                                                                                                                                                                                                                             |
| CreateDIBitmap    | O parâmetro fuUsage especifica que o membro bmiColors da estrutura BITMAPINFO apontada pelo parâmetro lpbmi ou não contém informações de cores. Se não tiver, nenhum gerenciamento de cores será executado para esse bitmap. O bitmap deve usar a versão 4 ou a versão 5 da estrutura BITMAPINFO para que o gerenciamento de cores seja habilitado. O conteúdo do bitmap resultante não é correspondente à cor após a criação do bitmap. |
| CreateDIBSection  | Se a estrutura BITMAPINFO passada pelo parâmetro pbmi não for a versão 4 ou 5, nenhum gerenciamento de cores será feito. Se for a versão 4 ou 5, o gerenciamento de cores será habilitado e o espaço de cores especificado será associado ao bitmap.                                                                                                                                                                                                   |
| MaskBlt           | Nenhum gerenciamento de cores é executado quando blits ocorre.                                                                                                                                                                                                                                                                                                                                                                                             |
| SelectObject      | Se o objeto for um bitmap criado com CreateDIBSection, o gerenciamento de cores será executado. O espaço de cores do bitmap é usado como o espaço de cores de destino.                                                                                                                                                                                                                                                                                       |
| SetDIBits         | O gerenciamento de cores é executado. Se a estrutura BITMAPINFO especificada não for a versão 4 ou 5, o perfil de cor do controlador de domínio atual será usado como o perfil de espaço de cor de origem. Se não tiver um, o espaço sRGB será usado. Se a estrutura BITMAPINFO especificada for a versão 4 ou 5, o perfil de espaço de cores especificado no cabeçalho de bitmap será usado como o perfil de espaço de cor de origem.                                         |
| SetDIBitsToDevice | O gerenciamento de cores é executado. Se a estrutura BITMAPINFO especificada não for a versão 4 ou 5, o perfil de cor do contexto do dispositivo atual será usado como o perfil de espaço de cor de origem. Se ele não tiver um, o espaço de cores sRGB será usado. Se a estrutura BITMAPINFO especificada for a versão 4 ou 5, o perfil de espaço de cores associado ao bitmap será usado como o espaço de cores de origem.                                    |
| SetDIBColorTable  | Nenhum gerenciamento de cores é executado.                                                                                                                                                                                                                                                                                                                                                                                                              |
| StretchBlt        | Nenhum gerenciamento de cores é executado quando blits ocorre.                                                                                                                                                                                                                                                                                                                                                                                             |
| StretchDIBits     | O gerenciamento de cores é executado. Se a estrutura BITMAPINFO especificada não for a versão 4 ou 5, o perfil de cor do controlador de domínio atual será usado como o perfil de espaço de cor de origem. Se não tiver um, o espaço sRGB será usado. Se a estrutura BITMAPINFO especificada for a versão 4 ou 5, o perfil de espaço de cores especificado no cabeçalho de bitmap será usado como o perfil de espaço de cor de origem.                                         |



 

 

 




