---
title: Mensagem de EM_GETSTORYTYPE (RichEdit. h)
description: Obtém o tipo de história.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- controles de Windows de mensagem de EM_GETSTORYTYPE
topic_type:
- apiref
api_name:
- EM_GETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4e6d501fffca857e1e283f2678c1b42e5d3d12e587e51a3a58585041489f8b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048776"
---
# <a name="em_getstorytype-message"></a>\_Mensagem em GEThistóriatype

Obtém o tipo de história.


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice da história.

</dd> <dt>

*lParam* 
</dt> <dd>

Reservado deve ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o tipo de história, que pode ser um valor personalizado definido pelo cliente ou um dos seguintes valores:

<dl> <dt>

**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SEThistóriatype**](em-setstorytype.md)
</dt> <dt>

[**ITextStoryRanges:: item**](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





