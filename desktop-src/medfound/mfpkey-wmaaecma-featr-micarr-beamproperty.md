---
description: Especifica o que o DSP de Captura de Voz usa para processamento de matriz de microfone.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: MFPKEY_WMAAECMA_FEATR_MICARR_BEAM propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9a91cef7d270af37adc8fda9805d7bf275ef9877883ed8ff8cfdbf9e7a55e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953526"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a>Propriedade MFPKEY \_ WMAAECMA \_ \_ MICARR \_ MICE

Especifica o que o DSP de Captura de Voz usa para processamento de matriz de microfone.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="applies-to"></a>Aplica-se A

-   [DSP de Captura de Voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

De definir essa propriedade se o valor da propriedade [ \_ MFPKEY WMAAECMA \_ \_ MICARR MICARR \_ MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md) for MICARRAY \_ EXTERN \_ TAMBÉM.

Se o valor de [**MFPKEY \_ WMAAECMARAKR \_ \_ MICARR \_ MODE**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) for MICARRAY SINGLE BEAM, você poderá ler essa propriedade para consultar qual raio foi selecionado pelo \_ \_ DSP.

Essa propriedade pode ter os valores a seguir. Os valores estão em graus horizontais.



| Valor | Descrição              |
|-------|--------------------------|
| 0     | -50 graus.             |
| 1     | -40 graus.             |
| 2     | -30 graus.             |
| 3     | -20 graus.             |
| 4     | -10 graus.             |
| 5     | 0 graus (raio central). |
| 6     | 10 graus.              |
| 7     | 20 graus.              |
| 8     | 30 graus.              |
| 9     | 40 graus.              |
| 10    | 50 graus.              |



 

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

 

 
