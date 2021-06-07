---
title: Uso de funções GDI com WCS
description: Há várias funções na GDI (interface de dispositivo gráfico) que usam ou operam em dados de cores.
ms.assetid: a19ec8b9-11c9-4fde-a99a-7f4a112b49e7
keywords:
- WCS (Sistema de Cores do Windows), interface de dispositivo gráfico (GDI)
- WCS (Sistema de Cores do Windows), interface de dispositivo gráfico (GDI)
- gerenciamento de cores de imagem, GDI (interface de dispositivo gráfico)
- gerenciamento de cores, GDI (interface do dispositivo gráfico)
- colors,graphics device interface (GDI)
- GDI (graphics device interface)
- GDI (interface do dispositivo gráfico)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fad8445623efb8854e81e7e1569beab9ed4169b
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443647"
---
# <a name="using-gdi-functions-with-wcs"></a>Uso de funções GDI com WCS

Há várias funções na GDI (interface de dispositivo gráfico) que usam ou operam em dados de cores. Algumas estão habilitadas para uso com o WCS e outras não. As seguintes funções GDI são relevantes para o ICM:

-   [Funções de contexto de dispositivo com WCS](#device-context-functions-with-wcs)
-   [Funções de caneta e pincel com WCS](#pen-and-brush-functions-with-wcs)
-   [Funções de saída de texto com WCS](#text-output-functions-with-wcs)
-   [Funções bitmap com WCS](#bitmap-functions-with-wcs)

## <a name="device-context-functions-with-wcs"></a>Funções de contexto de dispositivo com WCS



|    Função                |   Descrição                                                                                                                                                                                                                              |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Createcompatibledc | Se o DC (contexto do dispositivo) passado para essa função por meio de seu parâmetro hdc estiver habilitado para ICM, o DC que a função cria também será habilitado para ICM. Os espaços de cor de origem e destino são especificados no DC. |
| Createdc           | O ICM pode ser habilitado definindo o membro dmICMMethod da estrutura DEVMODE apontada pelo parâmetro pInitData para o valor apropriado. Para obter detalhes, consulte a documentação no SDK da plataforma na estrutura DEVMODE.  |
| Resetdc            | O perfil de cor do contexto do dispositivo especificado pelo parâmetro hdc será redefinido com base nas informações na estrutura DEVMODE especificada pelo parâmetro lpInitData.                                                   |



 

## <a name="pen-and-brush-functions-with-wcs"></a>Funções de caneta e pincel com WCS



|    Função                |   Descrição                                                                                                                                                                                                                              |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Funções de pincel | Nenhum gerenciamento de cores é feito na criação do pincel. No entanto, o gerenciamento de cores será executado quando o pincel for selecionado em um DC habilitado para ICM. |
| Createpen       | Nenhum gerenciamento de cores é feito na criação da caneta. No entanto, o gerenciamento de cores será executado quando o pincel for selecionado em um DC habilitado para ICM.   |
| ExtCreatePen    | Nenhum gerenciamento de cores é feito na criação da caneta. No entanto, o gerenciamento de cores será executado quando o pincel for selecionado em um DC habilitado para ICM.   |
| SelectObject    | Se o objeto que está sendo selecionado for um pincel ou uma caneta, o gerenciamento de cores será executado.                                                              |
| SetDCBrushColor | O gerenciamento de cores será executado se o WCS estiver habilitado.                                                                                              |
| SetDCPenColor   | O gerenciamento de cores será executado se o WCS estiver habilitado.                                                                                              |



 

## <a name="text-output-functions-with-wcs"></a>Funções de saída de texto com WCS



|    Função                |   Descrição                                                                                                                                                                                                                              |
|--------------|--------------------------------------------------|
| Setbkcolor   | O gerenciamento de cores será executado se o WCS estiver habilitado. |
| Settextcolor | O gerenciamento de cores será executado se o WCS estiver habilitado. |



 

## <a name="bitmap-functions-with-wcs"></a>Funções bitmap com WCS



|    Função                |   Descrição                                                                                                                                                                                                                              |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitblt            | Nenhum gerenciamento de cores é executado quando ocorrem blits.                                                                                                                                                                                                                                                                                                                                                                                             |
| Createdibitmap    | O parâmetro fuUsage especifica que o membro bmiColors da estrutura BITMAPINFO apontado pelo parâmetro lpbmi contém ou não informações de cor. Caso não faça isso, nenhum gerenciamento de cores será executado para este bitmap. O bitmap deve usar a versão 4 ou a versão 5 da estrutura BITMAPINFO para que o gerenciamento de cores seja habilitado. O conteúdo do bitmap resultante não é de cor após a criação do bitmap. |
| Createdibsection  | Se a estrutura BITMAPINFO passada pelo parâmetro pbmi não for a versão 4 ou a versão 5, nenhum gerenciamento de cores será feito. Se for a versão 4 ou 5, o gerenciamento de cores será habilitado e o espaço de cores especificado será associado ao bitmap.                                                                                                                                                                                                   |
| Maskblt           | Nenhum gerenciamento de cores é executado quando ocorrem blits.                                                                                                                                                                                                                                                                                                                                                                                             |
| SelectObject      | Se o objeto for um bitmap criado com CreateDIBSection, o gerenciamento de cores será executado. O espaço de cores do bitmap é usado como o espaço de cores de destino.                                                                                                                                                                                                                                                                                       |
| Setdibits         | O gerenciamento de cores é executado. Se a estrutura BITMAPINFO especificada não for a versão 4 ou a versão 5, o perfil de cor do DC atual será usado como o perfil de espaço de cor de origem. Se ele não tiver um, o espaço sRGB será usado. Se a estrutura BITMAPINFO especificada for a versão 4 ou a versão 5, o perfil de espaço de cores especificado no header do bitmap será usado como o perfil de espaço de cor de origem.                                         |
| Setdibitstodevice | O gerenciamento de cores é executado. Se a estrutura BITMAPINFO especificada não for a versão 4 ou a versão 5, o perfil de cor do contexto do dispositivo atual será usado como o perfil de espaço de cor de origem. Se ele não tiver um, o espaço de cor sRGB será usado. Se a estrutura BITMAPINFO especificada for a versão 4 ou a versão 5, o perfil de espaço de cores associado ao bitmap será usado como o espaço de cor de origem.                                    |
| SetDIBColorTable  | Nenhum gerenciamento de cores é executado.                                                                                                                                                                                                                                                                                                                                                                                                              |
| Stretchblt        | Nenhum gerenciamento de cores é executado quando ocorrem blits.                                                                                                                                                                                                                                                                                                                                                                                             |
| Stretchdibits     | O gerenciamento de cores é executado. Se a estrutura BITMAPINFO especificada não for a versão 4 ou a versão 5, o perfil de cor do DC atual será usado como o perfil de espaço de cor de origem. Se ele não tiver um, o espaço sRGB será usado. Se a estrutura BITMAPINFO especificada for a versão 4 ou a versão 5, o perfil de espaço de cores especificado no header do bitmap será usado como o perfil de espaço de cor de origem.                                         |



 

 

 




