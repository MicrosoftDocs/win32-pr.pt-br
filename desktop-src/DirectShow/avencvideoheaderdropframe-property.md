---
description: Especifica o valor do sinalizador de descarte de quadros no cabeçalho do grupo de imagens (GOP).
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: Propriedade AVEncVideoHeaderDropFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ffd9cdcfee05a52803c19216e62f7d51d52248bcc2bdc4ad0ad7d2b45293989
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342476"
---
# <a name="avencvideoheaderdropframe-property"></a>Propriedade AVEncVideoHeaderDropFrame

Especifica o valor do sinalizador de descarte de quadros no cabeçalho do grupo de imagens (GOP).

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoHeaderDropFrame**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade pode ser 0 ou 1.

## <a name="remarks"></a>Comentários

O modo de descarte de quadros é usado no vídeo NTSC para corrigir a discrepância entre o vídeo, que é de 29,97 quadros por segundo e a exibição do código de tempo, que é de 30 quadros por segundo. No modo de descarte de quadros, os números de quadro 00 e 01 são ignorados no início de cada minuto, exceto em minutos que são até múltiplos de dez (00, 10, 20 e assim por diante). Somente os números de quadro no código de tempo são descartados; nenhum quadro real foi removido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




