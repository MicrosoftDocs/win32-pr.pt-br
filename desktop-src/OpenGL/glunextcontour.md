---
title: função gluNextContour (Glu. h)
description: A função gluNextContour marca o início de outra delimitação.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- função gluNextContour OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4607fbeea8e8aa46b365204bf1853c392c1a38f5ded594d840c6e9eea063da2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061594"
---
# <a name="glunextcontour-function"></a>função gluNextContour

\[A função **gluNextContour** é obsoleta e é fornecida somente para fins de compatibilidade com versões anteriores. A função **gluNextContour** é mapeada para [**GluTessEndContour**](glutessendcontour.md) seguida por [**gluTessBeginContour**](glutessbegincontour.md).\]

A função **gluNextContour** marca o início de outra delimitação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tess* 
</dt> <dd>

O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo da delimitação que está sendo definida. Os valores a seguir são válidos.



| Valor                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <dt>**\_exterior Glu**</dt> </dl>           | Uma delimitação exterior define um limite exterior do polígono.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <dt>**GLU \_ interior**</dt> </dl>           | Uma delimitação interior define um limite interior do polígono (como uma brecha).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <dt>**GLU \_ desconhecido**</dt> </dl>              | Uma delimitação desconhecida é analisada pela biblioteca para determinar se ela é interior ou exterior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <dt>**GLU \_ CCW, glu \_ CW**</dt> </dl> | A primeira \_ contorno Glu CCW ou Glu \_ CW definida é considerada exterior. Todas as outras contornos serão consideradas exteriores se forem orientadas na mesma direção (no sentido horário ou anti-horário) como a primeira contorno e interior se não forem.<br/> Se uma delimitação for do tipo GLU \_ CCW ou Glu \_ CW, todos os contornos deverão ser do mesmo tipo (se não forem, todos os Glu \_ CCW e Glu \_ contornos em PV serão alterados para Glu \_ desconhecido). Observe que não há nenhuma diferença real entre os \_ tipos de contorno Glu CCW e Glu \_ CW.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use a função **gluNextContour** para descrever polígonos com vários contornos. Depois de descrever a primeira delimitação por meio de uma série de chamadas [**gluTessVertex**](glutessvertex.md) , uma chamada **gluNextContour** indica que a delimitação anterior foi concluída e que a próxima delimitação está prestes a começar. Execute outra série de chamadas **gluTessVertex** para descrever a nova delimitação. Repita esse processo até que todos os contornos tenham sido descritos.

O parâmetro de *tipo* define o tipo de delimitação a seguir.

Para definir o tipo da primeira delimitação, você pode chamar **gluNextContour** antes de descrever a primeira delimitação. Se você não chamar **gluNextContour** antes da primeira delimitação, a primeira delimitação será marcada como \_ exterior Glu.

## <a name="examples"></a>Exemplos

Você pode descrever um diamante com um buraco triangular, da seguinte maneira:

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4);  
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7);  
gluEndPolygon(tess);
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>GLU. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





