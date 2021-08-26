---
description: Contém o CLSID de um carregador de topologia para a sessão de mídia.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: Atributo MF_SESSION_TOPOLOADER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9568193bbdbd46485015b6e5975db26fca2b552b23b7c227576e4e6544d69af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955125"
---
# <a name="mf_session_topoloader-attribute"></a>\_Atributo TOPOLOADER da sessão MF \_

Contém o CLSID de um carregador de topologia para a sessão de mídia.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Você pode usar esse atributo para fornecer um carregador de topologia personalizado para a sessão de mídia.

Defina esse atributo usando o parâmetro *pConfiguration* da função [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou a função [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Se esse atributo for definido, a sessão de mídia chamará **CoCreateInstance** com o CLSID especificado quando ele criar o carregador de topologia. O objeto criado por esse CLSID deve expor a interface [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .

Se esse atributo não for definido, a sessão de mídia criará o carregador de topologia padrão fornecido no Media Foundation.

Um carregador de topologia deve dar suporte A Apartments multi-threaded. Você deve registrar o carregador de topologia como ThreadingModel = "both". Além disso, se você estiver usando o carregador de topologia dentro do caminho de mídia protegido (PMP), o carregador de topologia deverá ser um componente confiável. Para obter mais informações, consulte [proteção de caminho de mídia](protected-media-path.md).

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Atributos de sessão de mídia](media-session-attributes.md)
</dt> <dt>

[Carregadores de topologia personalizados](custom-topology-loaders.md)
</dt> </dl>

 

 




