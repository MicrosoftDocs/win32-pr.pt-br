---
description: Contém um ponteiro para a interface IMFNetProxyLocatorFactory.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: Propriedade MFNETSOURCE_PROXYLOCATORFACTORY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1199333e9eb343ab9d8f96864372b2dc385ab7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091152"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a>\_Propriedade MFNETSOURCE PROXYLOCATORFACTORY

Contém um ponteiro para a interface [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Ponteiro **IUnknown**

VT \_ desconhecido

**punkVal**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PROXYLOCATORFACTORY** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Os aplicativos podem usar essa propriedade para fornecer um localizador de proxy personalizado para a origem da rede. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Suporte de proxy para fontes de rede](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




