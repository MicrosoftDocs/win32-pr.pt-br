---
description: Contém o CLSID de um Gerenciador de qualidade para a sessão de mídia.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: Atributo MF_SESSION_QUALITY_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296980"
---
# <a name="mf_session_quality_manager-attribute"></a>\_Atributo do \_ Gerenciador de qualidade de sessão MF \_

Contém o CLSID de um Gerenciador de qualidade para a sessão de mídia.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Você pode usar esse atributo para fornecer um Gerenciador de qualidade personalizado para a sessão de mídia.

Defina esse atributo usando o parâmetro *pConfiguration* da função [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Se esse atributo for definido, a sessão de mídia chamará **CoCreateInstance** com o CLSID especificado para criar o Gerenciador de qualidade. O objeto criado por esse CLSID deve expor a interface [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) .

Se esse atributo não for definido, a sessão de mídia criará o Gerenciador de qualidade padrão fornecido no Media Foundation.

Se você quiser executar a sessão de mídia sem nenhum Gerenciador de qualidade, defina este atributo como **GUID \_ NULL**.

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

[**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Atributos de sessão de mídia](media-session-attributes.md)
</dt> </dl>

 

 




