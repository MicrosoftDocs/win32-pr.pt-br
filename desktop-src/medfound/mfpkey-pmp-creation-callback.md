---
description: Define um retorno de chamada que cria a sessão de mídia do PMP durante a resolução da origem.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: Propriedade MFPKEY_PMP_Creation_Callback (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165379"
---
# <a name="mfpkey_pmp_creation_callback-property"></a>\_Propriedade de \_ retorno de chamada de criação do MFPKEY PMP \_

Define um retorno de chamada que cria a [sessão de mídia do PMP](pmp-media-session.md) durante a resolução da origem.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**IUnknown \** _

VT \_ desconhecido

_ *punkVal**



## <a name="remarks"></a>Comentários

Um conteúdo protegido pode exigir o uso dessa propriedade. Nesse caso, o processo de resolução de origem falha com o código de erro **MF \_ E a \_ resolução \_ requer o retorno de chamada de \_ \_ criação \_ de PMP**.

Para usar essa propriedade, faça o seguinte.

1.  Chame [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para criar um repositório de propriedades.
2.  Implemente a interface de retorno de chamada [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
3.  Defina a propriedade de retorno de chamada de criação do MFPKEY \_ PMP \_ \_ no repositório de propriedades. O valor é um ponteiro para a implementação de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
4.  Chame [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl). Passe um ponteiro para o repositório de propriedades no parâmetro *pProps* .

No método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) da sua interface de retorno de chamada, faça o seguinte.

1.  Chame [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) para criar a [sessão de mídia do PMP](pmp-media-session.md).
2.  Chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) na sessão de mídia do PMP para um ponteiro para a interface [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) .
3.  Chame [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) no objeto result que é passado no parâmetro *pAsyncResult* de [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Consulte o ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) retornado para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
4.  Chame [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) com os seguintes parâmetros:
    -   *dwQueue*: **MFASYNC de \_ fila de retorno de chamada \_ \_ padrão**
    -   *pCallback*: o ponteiro [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) obtido na etapa 3.
    -   *pState*: o ponteiro [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) obtido na etapa 2.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Sessão de mídia do PMP](pmp-media-session.md)
</dt> <dt>

[Caminho de mídia protegido](protected-media-path.md)
</dt> <dt>

[Resolvedor de origem](source-resolver.md)
</dt> </dl>

 

 
