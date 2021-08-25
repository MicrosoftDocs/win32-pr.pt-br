---
description: Especifica se o DSP de Captura de Voz armazena estatísticas de carimbo de data/hora no Registro.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: MFPKEY_WMAAECMA_RETRIEVE_TS_STATS propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c28f9812bb5f1324fcb1153b84f5a6704c7481c8356073fd02b8d95b57a8e497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953496"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a>Propriedade MFPKEY \_ WMAAECMA \_ RETRIEVE \_ TS \_ STATS

Especifica se o DSP de Captura de Voz armazena estatísticas de carimbo de data/hora no Registro.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

BOOL da VT \_

## <a name="default-value"></a>Valor padrão

VARIANT \_ FALSE

## <a name="applies-to"></a>Aplica-se A

-   [DSP de Captura de Voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

Os algoritmos de AEC (cancelamento de eco acústico) dependem de carimbos de data/hora precisos nos fluxos de áudio. Na realidade, os carimbos de data/hora geralmente são defeitos e diferentes dispositivos de áudio podem apresentar taxas diferentes de variação e desacordo. Quando o AEC está habilitado, o DSP coleta estatísticas sobre os carimbos de data/hora e usa essas informações para compensar imprecisões.

Se o valor dessa propriedade for VARIANT TRUE, o DSP salvará as estatísticas que \_ coleta no Registro. Na próxima vez que o DSP executar o AEC usando o mesmo par de dispositivos de áudio, ele lerá as informações estatísticas do Registro, o que permite que o DSP execute com mais eficiência.

Se você definir o valor dessa propriedade como VARIANT TRUE e estiver usando o DSP no modo de filtro, também deverá definir a propriedade \_ [GUID MFPKEY \_ WMAAECMA \_ DEVICEPAIR. \_ ](mfpkey-wmaaecma-devicepair-guidproperty.md) No modo de origem, isso não é necessário.

O valor padrão dessa propriedade é VARIANT \_ FALSE. O DSP usa essa propriedade somente quando o processamento do AEC está habilitado.

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

 

 
