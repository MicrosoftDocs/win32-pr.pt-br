---
description: Especifica qual transmissão o DSP de captura de voz usa para processamento de matriz de microfone.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: Propriedade MFPKEY_WMAAECMA_FEATR_MICARR_BEAM (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759871"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a>\_Propriedade de \_ \_ \_ transmissão MICARR do MFPKEY WMAAECMA

Especifica qual transmissão o DSP de captura de voz usa para processamento de matriz de microfone.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

Defina essa propriedade se o valor da propriedade [do \_ \_ \_ \_ modo MICARR do MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-micarr-modeproperty.md) for MICARRAY de \_ \_ transmissão externa.

Se o valor de [**MFPKEY \_ WMAAECMA do \_ \_ \_ modo MICARR**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) for MICARRAY \_ Single \_ feixe, você poderá ler essa propriedade para consultar qual feixe foi selecionado pelo DSP.

Essa propriedade pode ter os valores a seguir. Os valores estão em graus horizontal.



| Valor | Descrição              |
|-------|--------------------------|
| 0     | -50 graus.             |
| 1     | -40 graus.             |
| 2     | -30 graus.             |
| 3     | -20 graus.             |
| 4     | -10 graus.             |
| 5     | 0 graus (feixe central). |
| 6     | 10 graus.              |
| 7     | 20 graus.              |
| 8     | 30 graus.              |
| 9     | 40 graus.              |
| 10    | 50 graus.              |



 

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

 

 
