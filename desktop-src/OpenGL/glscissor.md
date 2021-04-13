---
title: função glScissor (GL. h)
description: A função glScissor define a caixa de tesoura.
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- função glScissor OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e18559bb30260dcb4285980d8dc75642a7c9ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455951"
---
# <a name="glscissor-function"></a>função glScissor

A função **glScissor** define a caixa de tesoura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* 
</dt> <dd>

A coordenada x (eixo vertical) para o canto inferior esquerdo da caixa de tesoura.

</dd> <dt>

*y* 
</dt> <dd>

A coordenada y (eixo horizontal) para o canto inferior esquerdo da caixa de tesoura. Juntos, x e y especificam o canto inferior esquerdo da caixa de tesoura. Inicialmente (0, 0).

</dd> <dt>

*width* 
</dt> <dd>

A largura da caixa de tesoura.

</dd> <dt>

*altura* 
</dt> <dd>

A altura da caixa de tesoura. Quando um contexto OpenGL é anexado *pela primeira vez* a uma janela, a *largura* e a *altura* são definidas para as dimensões dessa janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | A *largura* ou a *altura* era negativa.<br/>                                                                                   |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glScissor** define um retângulo, chamado de caixa de tesoura, em coordenadas de janela. Os dois primeiros parâmetros, *x* e *y*, especificam o canto inferior esquerdo da caixa. Os parâmetros *Width* e *Height* especificam a largura e a altura da caixa.

O teste de recorte está habilitado e desabilitado usando [**glEnable**](glenable.md) e **glDisable** com o teste de recorte do Argument GL \_ \_ . Enquanto o teste de tesoura está habilitado, somente os pixels que estão na caixa de recorte podem ser modificados por comandos de desenho. As coordenadas da janela têm valores inteiros nos cantos compartilhados de framebuffer pixels, portanto, **glScissor**(0, 0, 1, 1) permite que apenas o pixel inferior esquerdo na janela seja modificado e **glScissor**(0, 0, 0, 0) não permita a modificação em todos os pixels na janela.

Quando o teste de tesoura é desabilitado, é como se a caixa de corte incluir a janela inteira.

As funções a seguir recuperam informações relacionadas ao **glScissor**:

caixa de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL de \_ mola \_

teste de recorte de [**glIsEnabled**](glisenabled.md) com Argument GL \_ \_

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





