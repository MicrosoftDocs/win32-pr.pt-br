---
description: Especifica se o codec deve tentar detectar bordas de quadro ruidosas e removê-las.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: Propriedade MFPKEY_NOISEEDGEREMOVAL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165385"
---
# <a name="mfpkey_noiseedgeremoval-property"></a>\_Propriedade MFPKEY NOISEEDGEREMOVAL

Especifica se o codec deve tentar detectar bordas de quadro ruidosas e removê-las.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCNoiseEdgeRemoval

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="default-value"></a>Valor padrão

FALSE

## <a name="remarks"></a>Comentários

Uma borda de quadro ruidosa é geralmente os dados de intervalo vertical em branco (VBI) de um quadro de televisão de difusão. O VBI é o primeiro 21 linhas de varredura do quadro de televisão. Essas linhas de varredura não contêm dados de vídeo — elas contêm dados sobre a transmissão. Quando um sinal de televisão é gravado por um cartão de captura, o VBI normalmente é removido do quadro. A detecção de borda ruidosa e a correção executada pelo codec só podem corrigir uma borda com três ou menos linhas de ruído. Se o vídeo capturado contiver mais de três linhas com ruído, haverá um problema com o hardware usado para capturar o vídeo.

Se o codec for definido para remover bordas ruidosas, ele duplicará as linhas adjacentes à borda ruidosa para preencher o quadro.

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

 

 




