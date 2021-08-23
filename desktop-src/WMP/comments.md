---
title: Comentários (msfeeds. h)
description: Adicione comentários a metaarquivos seguindo a sintaxe linguagem XML (XML). Os comentários começam com \ 0034; --\ 0034; e terminar com \ 0034;--\ 0034;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- Comentários Windows Media Player
topic_type:
- apiref
api_name:
- Comments
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fe5aaf9dde3d804bb91a1e2551636c86aa54ff2bec599bf06100ee2622b592a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135779"
---
# <a name="comments-msfeedsh"></a>Comentários (msfeeds. h)

Adicione comentários a metaarquivos seguindo a sintaxe linguagem XML (XML). Os comentários começam com " &lt; !--" e terminam com "-- &gt; ".

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a>Comentários

Os comentários podem aparecer em qualquer lugar, exceto no conteúdo do elemento (entre marcas de abertura e fechamento do elemento,  < >). Eles não fazem parte dos dados de caracteres do documento e são ignorados quando o metarquivo é analisado.

## <a name="examples"></a>Exemplos


```XML
<ASX version = "3.0">
<!-- This information is only visible when editing a metafile file. -->
<!--<BANNER HREF="c:\wmsdk\wmssdk\samples\dhtml\asfbutton3.gif">
    </BANNER>-->
    <ENTRY>
        <REF HREF = "mms://proseware.com/pubpt/filename.asf" />
    </ENTRY>

    <ENTRY>
        <TITLE>WMA Port na Pucai</TITLE>
        <!--<DURATION VALUE="00:00:15"/>-->
        <REF href="c:\asfroot\Port na Pucai.wma"/>
    </ENTRY></ASX>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Windows Referência de elementos de metarquivo de mídia**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





