---
description: Fornece uma interface de retorno de chamada para que o aplicativo receba um objeto de habilitação de conteúdo da sessão do caminho de mídia protegido (PMP).
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: Atributo MF_SESSION_CONTENT_PROTECTION_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788708"
---
# <a name="mf_session_content_protection_manager-attribute"></a>\_ \_ \_ Atributo Gerenciador de proteção de conteúdo de sessão MF \_

Fornece uma interface de retorno de chamada para que o aplicativo receba um objeto de habilitação de conteúdo da sessão do caminho de mídia protegido (PMP).

## <a name="data-type"></a>Tipo de dados

**IUnknown \** _

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [_ *IMFContentProtectionManager* *](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) do aplicativo.

Defina esse atributo na sessão do PMP usando o parâmetro *pConfiguration* da função [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Atributos de sessão de mídia](media-session-attributes.md)
</dt> <dt>

[Como reproduzir arquivos de mídia protegidos](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




