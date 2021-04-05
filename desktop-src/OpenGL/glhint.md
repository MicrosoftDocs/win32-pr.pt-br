---
title: função glHint (GL. h)
description: A função glHint especifica dicas específicas de implementação.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- função glHint OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2772c76868c741660486184e5ab51bd193d3667a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085322"
---
# <a name="glhint-function"></a>função glHint

A função **glHint** especifica dicas específicas de implementação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

Uma constante simbólica que indica o comportamento a ser controlado. As constantes simbólicas a seguir, juntamente com a semântica sugerida, são aceitas.



| Valor                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <dt>**\_dica de neblina GL \_**</dt> </dl>                                                           | Indica a precisão do cálculo de neblina. Se o cálculo de neblina por pixel não for compatível com eficiência pela implementação do OpenGL, a dica GL não se \_ \_ preocupa ou o GL \_ mais rápido pode resultar no cálculo por vértice de efeitos de neblina.<br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <dt>**\_ \_ dica Smooth de linha gl \_**</dt> </dl>                                  | Indica a qualidade de amostragem de linhas AntiAlias. O Hint GL \_ mais interessante pode resultar em mais fragmentos de pixel sendo gerados durante a rasterização, se uma função de filtro maior for aplicada.<br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <dt>**\_dica de \_ correção de perspectiva GL \_**</dt> </dl> | Indica a qualidade da cor e a interpolação de coordenadas de textura. Se a interpolação de parâmetro com correção de perspectiva não tiver suporte eficiente pela implementação do OpenGL, a dica GL não \_ \_ cuidará ou o GL \_ mais rápido poderá resultar em uma interpolação linear simples de cores e/ou coordenadas de textura.<br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <dt>**\_ \_ dica Smooth do ponto GL \_**</dt> </dl>                               | Indica a qualidade de amostragem de pontos AntiAlias. O Hint GL \_ mais interessante pode resultar em mais fragmentos de pixel sendo gerados durante a rasterização, se uma função de filtro maior for aplicada.<br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <dt>**\_dica de \_ suavização do polígono GL \_**</dt> </dl>                         | Indica a qualidade de amostragem de polígonos com alias. O Hint GL \_ mais interessante pode resultar em mais fragmentos de pixel sendo gerados durante a rasterização, se uma função de filtro maior for aplicada.<br/>                                                                                                            |



 

</dd> <dt>

*mode* 
</dt> <dd>

Uma constante simbólica que indica o comportamento desejado. As constantes simbólicas a seguir são aceitas.



| Valor                                                                                                                                                       | Significado                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <dt>**GL \_ mais rápido**</dt> </dl>        | A opção mais eficiente deve ser escolhida.<br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <dt>**GL mais \_ interessante**</dt> </dl>           | A opção mais correta ou de qualidade mais alta deve ser escolhida.<br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <dt>**GL não se \_ \_ preocupa**</dt> </dl> | O cliente não tem uma preferência.<br/>                          |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *destino* ou o *modo* não era um valor aceito.<br/>                                                                              |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Quando há espaço para interpretação, você pode controlar determinados aspectos do comportamento do OpenGL com dicas. Você especifica uma dica com dois argumentos. O parâmetro de *destino* é uma constante simbólica que indica o comportamento a ser controlado e o *modo* é outra constante simbólica que indica o comportamento desejado.

Embora os aspectos de implementação que podem ser indicados sejam bem definidos, a interpretação das dicas depende da implementação.

A função **glHint** pode ser ignorada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





