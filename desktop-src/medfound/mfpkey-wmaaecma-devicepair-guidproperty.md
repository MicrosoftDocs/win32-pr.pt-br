---
description: Identifica a combinação de dispositivos de áudio que o aplicativo está usando no momento com o DSP de captura de voz.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: Propriedade MFPKEY_WMAAECMA_DEVICEPAIR_GUID (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174bbae3c83ef28ece7d05e36b0a05813078a9a9fba73ac7fae7dba25b67fb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973325"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a>\_Propriedade MFPKEY WMAAECMA \_ DEVICEPAIR \_ GUID

Identifica a combinação de dispositivos de áudio que o aplicativo está usando no momento com o DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

CLSID do VT \_

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

Defina essa propriedade se você estiver usando o DSP no modo de filtro e o valor da propriedade [MFPKEY \_ WMAAECMA \_ recuperar \_ TS \_ stats](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) for Variant \_ true.

Quando a propriedade [**MFPKEY \_ WMAAECMA \_ recuperar \_ TS \_ stats**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) é Variant \_ true, o DSP coleta estatísticas sobre os carimbos de data/hora dos dispositivos de áudio e armazena essas informações no registro. Essas estatísticas podem ser alteradas para cada combinação de dispositivo de captura de áudio e dispositivo de renderização de áudio. Portanto, o aplicativo deve atribuir um GUID para identificar a combinação específica de dispositivos em uso. O aplicativo deve manter o controle desse GUID, para que ele possa atribuir o mesmo GUID sempre que usar o mesmo par de dispositivos de áudio.

Se você estiver usando o DSP no modo de origem, não será necessário definir essa propriedade. O DSP gera automaticamente um GUID com base no valor da propriedade [de \_ \_ \_ índices de dispositivo MFPKEY WMAAECMA](mfpkey-wmaaecma-device-indexesproperty.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
