---
description: Contém um ponteiro para a interface IMFNetProxyLocatorFactory.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: MFNETSOURCE_PROXYLOCATORFACTORY propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc06f58fc11e4d0dcff95274170a76b25160b584231bd2c9e39ed1949b1363e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954736"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a>Propriedade MFNETSOURCE \_ PROXYLOCATORFACTORY

Contém um ponteiro para a interface [**IMFNetProxyLocatorFactory.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory)



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**Ponteiro IUnknown**

VT \_ UNKNOWN

**quevalVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PROXYLOCATORFACTORY** define o GUID para essa chave de propriedade. O PID (identificador de propriedade) é zero.

Os aplicativos podem usar essa propriedade para fornecer um localizador de proxy personalizado para a origem da rede. Para definir a propriedade , passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Suporte a proxy para fontes de rede](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




