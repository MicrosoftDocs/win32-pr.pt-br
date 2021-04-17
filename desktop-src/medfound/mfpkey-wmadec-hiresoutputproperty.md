---
description: Especifica se o decodificador de áudio deve fornecer saída de alta resolução.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: Propriedade MFPKEY_WMADEC_HIRESOUTPUT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762345"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a>\_Propriedade MFPKEY WMADEC \_ HIRESOUTPUT

Especifica se o decodificador de áudio deve fornecer saída de alta resolução.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACHiResOutput

## <a name="data-type"></a>Tipo de Dados

**BOOL do VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANTE \_ falso**

## <a name="remarks"></a>Comentários

Defina essa propriedade como VARIANT \_ true para decodificar o conteúdo de áudio de multicanais ou de 24 bits, ou áudio com uma taxa de exemplo maior que 48.000 Hz. Se o conteúdo for codificado em alta resolução, mas essa propriedade for VARIANT \_ false, os seguintes comportamentos se aplicarão:

-   A saída de DMO será limitada a estéreo de 16 bits, 48-KHz.
-   O MFT enumerará modos de saída limitados a 16 bits e não envolverá alterações na contagem de canais ou na taxa de amostragem.

As propriedades de áudio de alta resolução são passadas em uma estrutura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) , não [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).

A saída de alta resolução estará disponível somente se o decodificador estiver em execução no Windows XP ou posterior. Você pode definir essa propriedade independentemente do sistema operacional no qual seu aplicativo está sendo executado. Nas versões do Windows anteriores ao Windows XP, o decodificador ignorará essa configuração e entregará a saída padrão.

Muitos players (incluindo o Windows Media Player 9 Series e posterior) definem esse valor para todo o conteúdo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
