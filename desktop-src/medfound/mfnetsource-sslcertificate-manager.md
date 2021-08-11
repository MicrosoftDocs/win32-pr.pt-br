---
description: Armazena o ponteiro IUnknown da classe que implementa a interface IMFSSLCertificateManager.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: MFNETSOURCE_SSLCERTIFICATE_MANAGER propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6f853ae3fe44a9c4508386df4096e4adac36f3cec8a8cf199eb91cb87e1fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243290"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a>Propriedade MFNETSOURCE \_ SSLCERTIFICATE \_ MANAGER

Armazena o **ponteiro IUnknown** da classe que implementa a interface [**IMFSSLCertificateManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) A implementação do cliente fornece métodos para obter o certificado SSL do cliente quando ele é solicitado pelo servidor.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**Ponteiro IUnknown**

VT \_ UNKNOWN

**quevalVal**



## <a name="remarks"></a>Comentários

A **constante MFNETSOURCE \_ SSLCERTIFICATE \_ MANAGER** define o GUID para a chave de propriedade. O PID (identificador de propriedade) é zero. Para definir essa propriedade na origem da rede, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




