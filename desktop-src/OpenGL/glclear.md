---
title: função glClear (GL. h)
description: A função glClear limpa os buffers para valores predefinidos.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- função glClear OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb48a1b2832a5f9c046bb450b7cfba9ec4f83a759b093df91f3ec2064f23a3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082096"
---
# <a name="glclear-function"></a>função glClear

A função **glClear** limpa os buffers para valores predefinidos.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mask* 
</dt> <dd>

Os operadores or de máscaras que indicam os buffers a serem apagados. As quatro máscaras são as seguintes.



| Valor                                                                                                                                                                                   | Significado                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <dt>**\_bit do \_ buffer de cores GL \_**</dt> </dl>       | Os buffers atualmente estão habilitados para gravação de cores.<br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <dt>**\_bit de \_ buffer de profundidade GL \_**</dt> </dl>       | O buffer de profundidade.<br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <dt>**BIT de buffer do GL \_ Accum \_ \_**</dt> </dl>       | O buffer de acumulação.<br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <dt>**\_bit de \_ buffer do estêncil GL \_**</dt> </dl> | O buffer de estêncil.<br/>                              |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | Um pouco além dos quatro bits definidos foi definido em *Mask*.<br/>                                                                |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glClear** define a área Bitplane da janela para os valores selecionados anteriormente por [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)e [**glClearAccum**](glclearaccum.md). Você pode limpar vários buffers de cores simultaneamente selecionando mais de um buffer por vez usando [**glDrawBuffer**](gldrawbuffer.md).

O teste de propriedade de pixel, o teste de tesoura, o pontilhamento e o buffer writemasks afetam a operação de **glClear**. A caixa de tesoura limita a região limpa. A função **glClear** ignora a função Alpha, a função Blend, a operação lógica, a estêncil, o mapeamento de textura e o buffer *z*.

A função **glClear** usa um único argumento (*Mask*) que é o bit a bit ou vários valores indicando qual buffer deve ser limpo.

O valor para o qual cada buffer é limpo depende da configuração do valor de limpeza para esse buffer.

Se um buffer não estiver presente, uma chamada **glClear** direcionada a esse buffer não terá nenhum efeito.

As funções a seguir recuperam informações relacionadas ao **glClear**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com argumento GL \_ Accum \_ valor de limpeza \_

**glGet** com \_ \_ valor claro de profundidade do argumento GL \_

**glGet** com o \_ \_ valor Clear do índice do Argument GL \_

**glGet** com o \_ valor de \_ limpeza de cor do argumento GL \_

**glGet** com o \_ valor de \_ limpeza do estêncil GL do argumento \_

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

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glClearColor**](glclearcolor.md)
</dt> <dt>

[**glClearDepth**](glcleardepth.md)
</dt> <dt>

[**glClearIndex**](glclearindex.md)
</dt> <dt>

[**glClearStencil**](glclearstencil.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> </dl>

 

 





