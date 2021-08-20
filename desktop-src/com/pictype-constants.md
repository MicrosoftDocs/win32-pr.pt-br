---
title: Constantes PICTYPE (OleCtl.h)
description: Descreva o tipo de um objeto de imagem retornado por IPicture get Type, bem como para descrever o tipo de imagem no membro picType da estrutura PICTDESC que é passada para \_ OleCreatePictureIndirect.
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa6ac7be72ba34616a1ae8d596efbad3af761760c8f5e5c2bfa5dc8362593748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567646"
---
# <a name="pictype-constants"></a>Constantes PICTYPE

Descreva o tipo de um objeto de imagem retornado por [**IPicture::get \_ Type,**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)bem como para descrever o tipo de imagem no membro **picType** da estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) que é passada para [**OleCreatePictureIndirect.**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)



| Constante/valor                                                                                                                                                                                                                                  | Descrição                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <dt>**PICTYPE \_ NÃO REINICIALIZADO**</dt> <dt>(-1)</dt> </dl> | No momento, o objeto de imagem não está reinicializado. Esse valor só é válido como um valor de retorno de [**IPicture::get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) e não é válido com a estrutura [**PICTDESC.**](/windows/win32/api/olectl/ns-olectl-pictdesc)<br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <dt>**PICTYPE \_ NONE**</dt> <dt>0</dt> </dl>                               | Um novo objeto de imagem deve ser criado sem um estado inicializado. Esse valor só é válido na estrutura [**PICTDESC.**](/windows/win32/api/olectl/ns-olectl-pictdesc)<br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <dt>**PICTYPE \_ BITMAP**</dt> <dt>1</dt> </dl>                         | O tipo de imagem é um bitmap. Quando esse valor ocorre na estrutura [**PICTDESC,**](/windows/win32/api/olectl/ns-olectl-pictdesc) isso significa que o **campo bmp** dessa estrutura contém os parâmetros de inicialização relevantes.<br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <dt>**PICTYPE \_ METAFILE**</dt> <dt>2</dt> </dl>                   | O tipo de imagem é um metadado. Quando esse valor ocorre na estrutura [**PICTDESC,**](/windows/win32/api/olectl/ns-olectl-pictdesc) isso significa que o campo **wmf** dessa estrutura contém os parâmetros de inicialização relevantes.<br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <dt>**PICTYPE \_ ÍCONE**</dt> <dt>3</dt> </dl>                               | O tipo de imagem é um ícone. Quando esse valor ocorre na estrutura [**PICTDESC,**](/windows/win32/api/olectl/ns-olectl-pictdesc) isso significa que o campo de ícone dessa estrutura contém os parâmetros de inicialização relevantes. <br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <dt>**PICTYPE \_ ENFILEAFILE**</dt> <dt>4</dt> </dl>          | O tipo de imagem é um metadado aprimorado. Quando esse valor ocorre na estrutura [**PICTDESC,**](/windows/win32/api/olectl/ns-olectl-pictdesc) isso significa que o campo **emf** dessa estrutura contém os parâmetros de inicialização relevantes.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>OleCtl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipo IPicture::get \_**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





