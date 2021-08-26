---
description: Especifica se o DSP de Captura de Voz aplica a delimitação de ganho de microfone.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d00e906ec953e2fd00d9c288336c322c2d0dc07ea1c2d74a014ab78ae21acd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113146"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a>Propriedade DELIMITADOR \_ MFPKEY WMAAECMA \_ MIC \_ GAIN \_

Especifica se o DSP de Captura de Voz aplica a delimitação de ganho de microfone.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

BOOL da VT \_

## <a name="default-value"></a>Valor padrão

VARIANT \_ TRUE

## <a name="applies-to"></a>Aplica-se A

-   [DSP de Captura de Voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

A delimitação de ganho de microfone garante que o microfone tenha o nível correto de ganho. Se o ganho for muito alto, o sinal capturado poderá estar saturado e será recortado. O recorte é um efeito não linear, o que fará com que o algoritmo AEC (cancelamento de eco acústico) falhe. Se o ganho for muito baixo, a taxa de sinal para ruído será baixa, o que também pode fazer com que o algoritmo AEC falhe ou não tenha um bom desempenho.

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição                       |
|----------------|-----------------------------------|
| VARIANT \_ TRUE  | Habilita a delimitação de ganho de microfone.  |
| VARIANT \_ FALSE | Desabilite a delimitação de ganho de microfone. |



 

O valor padrão dessa propriedade é VARIANT \_ TRUE (habilitado).

A delimitação do ganho de microfone só se aplica quando o DSP opera no modo de origem. No modo de filtro, o aplicativo deve garantir que o microfone tenha o nível de ganho correto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[DSP de Captura de Voz](voicecapturedmo.md)
</dt> </dl>

 

 
