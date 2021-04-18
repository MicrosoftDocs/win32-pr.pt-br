---
description: Especifica se o DSP de captura de voz aplica o limite de lucro do microfone.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: Propriedade MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c1b09f2095f5accb44e4e0edaff2b8c94941d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760600"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a>\_Propriedade do \_ \_ \_ limitador de MFPKEY WMAAECMA MIC

Especifica se o DSP de captura de voz aplica o limite de lucro do microfone.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="default-value"></a>Valor padrão

VARIANTE \_ true

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O limite de lucro do microfone garante que o microfone tenha o nível correto de lucro. Se o lucro for muito alto, o sinal capturado poderá ser saturado e será recortado. O recorte é um efeito não linear, o que fará com que o algoritmo de cancelamento de eco acústico (AEC) falhe. Se o lucro for muito baixo, a taxa de sinal para ruído é baixa, o que também pode fazer com que o algoritmo AEC falhe ou não funcione bem.

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição                       |
|----------------|-----------------------------------|
| VARIANTE \_ true  | Habilitar limite de lucro de microfone.  |
| VARIANTE \_ falso | Desabilitar limite de lucro de microfone. |



 

O valor padrão dessa propriedade é VARIANT \_ true (Enabled).

O limite de lucro do microfone é aplicado somente quando o DSP opera no modo de origem. No modo de filtro, o aplicativo deve garantir que o microfone tenha o nível de lucro correto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
