---
title: Mensagem de EM_GETSTORYTYPE (RichEdit. h)
description: Obtém o tipo de história.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- Controles de EM_GETSTORYTYPE de mensagens do Windows
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
ms.openlocfilehash: 7fed85183f292bd1c69e3bbebdadb4b38f9f3bdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824364"
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

## <a name="return-value"></a>Retornar valor

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SEThistóriatype**](em-setstorytype.md)
</dt> <dt>

[**ITextStoryRanges:: item**](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





