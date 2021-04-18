---
title: Constantes PICTYPE (OleCtl. h)
description: Descreva o tipo de um objeto de imagem como retornado pelo tipo Get IPicture \_ , bem como para descrever o tipo de imagem no membro picType da estrutura PICTDESC que é passada para OleCreatePictureIndirect.
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
ms.openlocfilehash: bebf8ad8f678e9b6e463ade9f149b2e1d4bab529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105807195"
---
# <a name="pictype-constants"></a>Constantes PICTYPE

Descreva o tipo de um objeto de imagem como retornado [**por IPicture:: \_ Get Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), bem como para descrever o tipo de imagem no membro **picType** da estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) que é passada para [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).



| Constante/valor                                                                                                                                                                                                                                  | Descrição                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <dt>**PICTYPE \_ Não INICIALIZAdo**</dt> <dt>(-1)</dt> </dl> | O objeto de imagem não foi inicializado no momento. Esse valor só é válido como um valor de retorno de [**IPicture:: get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) e não é válido com a estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .<br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <dt>**PICTYPE \_ NENHUM**</dt> <dt>0</dt> </dl>                               | Um novo objeto de imagem deve ser criado sem um estado inicializado. Esse valor é válido somente na estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .<br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <dt>**PICTYPE \_ BITMAP**</dt> <dt>1</dt> </dl>                         | O tipo de imagem é um bitmap. Quando esse valor ocorre na estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , isso significa que o campo **BMP** dessa estrutura contém os parâmetros de inicialização relevantes.<br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <dt>**PICTYPE \_ METARQUIVO**</dt> <dt>2</dt> </dl>                   | O tipo de imagem é um metarquivo. Quando esse valor ocorre na estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , isso significa que o campo **WMF** dessa estrutura contém os parâmetros de inicialização relevantes.<br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <dt>**PICTYPE \_ ÍCONE**</dt> <dt>3</dt> </dl>                               | O tipo de imagem é um ícone. Quando esse valor ocorre na estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , isso significa que o campo de **ícone** dessa estrutura contém os parâmetros de inicialização relevantes.<br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <dt>**PICTYPE \_ ENHMETAFILE**</dt> <dt>4</dt> </dl>          | O tipo de imagem é um metarquivo avançado. Quando esse valor ocorre na estrutura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , isso significa que o campo **EMF** dessa estrutura contém os parâmetros de inicialização relevantes.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>OleCtl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPicture:: obter \_ tipo**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





