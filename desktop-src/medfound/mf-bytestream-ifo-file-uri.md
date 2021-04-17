---
description: 'Contém a URL do arquivo IFO (informações de DVD) especificado pelo servidor HTTP no cabeçalho HTTP, &\# 0034; Pragma: ifoFileURI.dlna.org&\# 0034;.'
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: Atributo MF_BYTESTREAM_IFO_FILE_URI (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c80e015b68272b073c442b4064c80a6787b811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105792575"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a>\_Atributo de \_ \_ URI de arquivo MF bytes IFO \_

Contém a URL do arquivo IFO (informações de DVD) especificado pelo servidor HTTP no cabeçalho HTTP, "pragma: ifoFileURI.dlna.org".

## <a name="data-type"></a>Tipo de dados

**LPWSTR**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Aplica-se a

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Comentários

O fluxo de bytes HTTP pesquisa o cabeçalho HTTP para a cadeia de caracteres "ifoFileURI.dlna.org". Se a cadeia de caracteres for encontrada, ela será copiada para esse atributo no fluxo de bytes.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                                           |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de fluxo de bytes](byte-stream-attributes.md)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




