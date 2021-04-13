---
title: função glAddSwapHintRectWIN (GL. h)
description: A função de retorno de chamada glAddSwapHintRectWIN especifica um conjunto de retângulos que devem ser copiados pelo SwapBuffers.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- função glAddSwapHintRectWIN OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369703"
---
# <a name="gladdswaphintrectwin-function"></a>função glAddSwapHintRectWIN

A função de retorno de chamada **glAddSwapHintRectWIN** especifica um conjunto de retângulos que devem ser copiados pelo [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glAddSwapHintRectWIN(
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

A coordenada *x*(em coordenadas de janela) do canto inferior esquerdo do retângulo da região de dica.

</dd> <dt>

*y* 
</dt> <dd>

A coordenada *y*(em coordenadas de janela) do canto inferior esquerdo do retângulo da região de dica.

</dd> <dt>

*width* 
</dt> <dd>

A largura do retângulo da região de dica.

</dd> <dt>

*altura* 
</dt> <dd>

A altura do retângulo da região de dica.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **glAddSwapHintRectWIN** acelera a animação, reduzindo a quantidade de repintura entre quadros. Com o **glAddSwapHintRectWIN**, você especifica um conjunto de áreas retangulares que deseja copiar ao chamar [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). Quando você não especificar retângulos com **glAddSwapHintRectWIN** antes de chamar **SwapBuffers**, a framebuffer inteira será trocada. O uso de **glAddSwapHintRectWIN** para copiar apenas partes alteradas do buffer pode aumentar significativamente o desempenho do **SwapBuffers**, especialmente quando o **SwapBuffers** é implementado no software.

A função **glAddSwapHintRectWIN** adiciona um retângulo à região de dica. Quando o \_ \_ sinalizador de cópia de permuta PFD da estrutura de formato [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) pixel é definido, **SwapBuffers** usa essa região para recortar a cópia do buffer de fundo para o buffer frontal. Você não especifica \_ \_ a cópia de permuta PFD; ela é definida pelo hardware compatível. A região de dica é desmarcada após cada chamada para **SwapBuffers**. Com algumas configurações de hardware, o **SwapBuffers** pode ignorar a região de dicas e trocar o buffer inteiro. O **SwapBuffers** é implementado pelo sistema, não pelo aplicativo.

O OpenGL mantém uma região de dica separada para cada janela. Quando você chama **glAddSwapHintRectWIN** em quaisquer contextos de renderização associados a uma janela, os retângulos de dica são combinados em uma única região.

Chame **glAddSwapHintRectWIN** com um retângulo delimitador para cada objeto desenhado para um quadro e para cada retângulo limpo para apagar objetos de quadro anteriores.

> [!Note]  
> A função **glAddSwapHintRectWIN** é uma função de extensão que não faz parte da biblioteca OpenGL padrão, mas faz parte da \_ extensão de dica GL Win \_ swap \_ . Para verificar se a implementação do OpenGL dá suporte a **glAddSwapHintRectWIN**, chame **glGetString**( \_ extensões GL). Se retornar a \_ dica GL Win \_ swap \_ , **glAddSwapHintRectWIN** terá suporte. Para obter o endereço de uma função de extensão, chame **wglGetProcAddress**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





