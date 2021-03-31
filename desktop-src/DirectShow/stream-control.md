---
description: Controle de fluxo
ms.assetid: b529b38c-a25c-42dd-aee1-5d263c94202d
title: Controle de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41cee586737e131d4a32508b9ba6dd9ef1bd3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829067"
---
# <a name="stream-control"></a>Controle de fluxo

A interface [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) no PIN de entrada do VMR permite que os aplicativos e filtros upstream controlem o comportamento do componente do mixer, incluindo a ordem Z e o estado ativo dos fluxos de entrada do VMR. Embora essa interface seja exposta nos Pins, ela opera no componente mixer do VMR, portanto, ela só estará disponível quando o mixer for carregado, que é quando o VMR está processando vários fluxos de entrada. Os filtros upstream usam os métodos [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) e [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) para controlar a chave de cor de origem. Esses métodos permitem efeitos como a sobreposição de animação em vídeo. Basta definir a chave de cor como a cor do plano de fundo do fluxo de animação e o VMR vai misturar esse fluxo com outro fluxo de vídeo. Os aplicativos devem tomar cuidado para não alterar a chave de cores para algum valor que seja diferente do valor que está sendo usado por um filtro upstream, como um decodificador.

Os filtros usam os métodos [**GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) e [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) para informar ao mixer se os dados de entrada devem ser esperados de um PIN especificado. Por exemplo, o decodificador Line21 usa esses métodos para ativar o PIN de entrada do VMR para dados do Line21 somente quando esses dados estão presentes no fluxo. Definir um PIN como um estado inativo instrui o mixer a não aguardar dados de um PIN especificado antes de compor a imagem.

 

 



