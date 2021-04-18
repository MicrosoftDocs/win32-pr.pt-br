---
description: Indica se um fluxo contém conteúdo protegido.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: Atributo MF_SD_PROTECTED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c97320d15353b8e23a43fa4efac2e5883a7366f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793896"
---
# <a name="mf_sd_protected-attribute"></a>\_ \_ Atributo protegido do MF SD

Indica se um fluxo contém conteúdo protegido.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de fluxo. Se o valor do atributo for **true**, o fluxo conterá conteúdo protegido. Se o valor for **false** ou o atributo não estiver definido, o fluxo conterá limpar conteúdo.

Em vez de verificar cada fluxo para esse atributo, você pode passar um descritor de apresentação para a função [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) . Essa função testa se o descritor de apresentação contém quaisquer fluxos protegidos.

Uma fonte de mídia deve definir esse atributo no descritor de fluxo se o conteúdo exigir o caminho de mídia protegido (PMP).

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="examples"></a>Exemplos


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos do descritor de fluxo](stream-descriptor-attributes.md)
</dt> </dl>

 

 




