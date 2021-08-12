---
title: Função glAddSwapHintRectWIN (Gl.h)
description: A função de retorno de chamada glAddSwapHintRectWIN especifica um conjunto de retângulos que devem ser copiados por SwapBuffers.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- Função glAddSwapHintRectWIN OpenGL
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
ms.openlocfilehash: 75077ac2a93e3e952ae3c3daca3ea847f7b4b0efc340da0e980b1a4bec6efa64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618046"
---
# <a name="gladdswaphintrectwin-function"></a>Função glAddSwapHintRectWIN

A função de retorno de chamada **glAddSwapHintRectWIN** especifica um conjunto de retângulos que devem ser copiados por [**SwapBuffers.**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)

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

A *coordenada x*(em coordenadas de janela) do canto inferior esquerdo do retângulo da região de dica.

</dd> <dt>

*y* 
</dt> <dd>

A *coordenada y*(em coordenadas de janela) do canto inferior esquerdo do retângulo da região de dica.

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

A **função glAddSwapHintRectWIN** acelera a animação reduzindo a quantidade de reainting entre quadros. Com **glAddSwapHintRectWIN**, você especifica um conjunto de áreas retangulares que deseja copiar ao chamar [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). Quando você não especifica nenhum retângulo com **glAddSwapHintRectWIN** antes de chamar **SwapBuffers,** todo o framebuffer é trocado. Usar **glAddSwapHintRectWIN** para copiar apenas partes alteradas do buffer pode aumentar significativamente o desempenho de **SwapBuffers,** especialmente quando **SwapBuffers** é implementado no software.

A **função glAddSwapHintRectWIN** adiciona um retângulo à região de dica. Quando o sinalizador PFD SWAP COPY da estrutura de formato de \_ \_ pixel [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) é definido, **SwapBuffers** usa essa região para cortar a cópia do buffer de fundo para o buffer frontal. Você não especifica PFD \_ SWAP \_ COPY; ele é definido pelo hardware com capacidade. A região de dica é limpa após cada chamada para **SwapBuffers.** Com algumas configurações de hardware, **SwapBuffers** pode ignorar a região de dica e trocar todo o buffer. **SwapBuffers** é implementado pelo sistema, não pelo aplicativo.

O OpenGL mantém uma região de dica separada para cada janela. Quando você chama **glAddSwapHintRectWIN** em todos os contextos de renderização associados a uma janela, os retângulos de dica são combinados em uma única região.

Chame **glAddSwapHintRectWIN** com um retângulo delimitador para cada objeto desenhado para um quadro e para cada retângulo limpo para apagar objetos de quadro anteriores.

> [!Note]  
> A **função glAddSwapHintRectWIN** é uma função de extensão que não faz parte da biblioteca OpenGL padrão, mas faz parte da extensão de dica de troca GL \_ \_ \_ WIN. Para verificar se sua implementação do OpenGL dá suporte **a glAddSwapHintRectWIN**, chame **glGetString**(GL \_ EXTENSIONS). Se ele retornar a \_ dica de troca GL \_ \_ WIN, **glAddSwapHintRectWIN** será suportado. Para obter o endereço de uma função de extensão, chame **wglGetProcAddress**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl> |



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

 

 





