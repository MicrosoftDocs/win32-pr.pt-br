---
description: Especifica se o DSP de captura de voz armazena estatísticas de carimbo de data/hora no registro.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: Propriedade MFPKEY_WMAAECMA_RETRIEVE_TS_STATS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810687"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a>MFPKEY \_ WMAAECMA \_ recuperar \_ \_ Propriedade TS stats

Especifica se o DSP de captura de voz armazena estatísticas de carimbo de data/hora no registro.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="default-value"></a>Valor padrão

VARIANTE \_ falso

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

Os algoritmos de cancelamento de eco acústico (AEC) dependem de carimbos de data/hora precisos nos fluxos de áudio. Na realidade, os carimbos de data/hora geralmente são imperfeitos e diferentes dispositivos de áudio podem apresentar taxas diferentes de variação e descompasso. Quando o AEC está habilitado, o DSP coleta estatísticas sobre os carimbos de data e hora e usa essas informações para compensar as imprecisões.

Se o valor dessa propriedade for VARIANT \_ true, o DSP salvará as estatísticas coletadas no registro. Na próxima vez que o DSP executar o AEC usando o mesmo par de dispositivos de áudio, ele lerá as informações estatísticas do registro, o que permite que o DSP seja executado com mais eficiência.

Se você definir o valor dessa propriedade como VARIANT \_ true e estiver usando o DSP no modo de filtro, também deverá definir a propriedade [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) . No modo de origem, isso não é necessário.

O valor padrão dessa propriedade é VARIANT \_ false. O DSP usa essa propriedade somente quando o processamento de AEC está habilitado.

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

 

 
