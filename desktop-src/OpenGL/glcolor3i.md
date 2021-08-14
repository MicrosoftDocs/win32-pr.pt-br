---
title: Função glColor3i (Gl.h)
description: Define a cor atual. | Função glColor3i (Gl.h)
ms.assetid: 9c68221b-1633-435b-9ae4-abc1c52601aa
keywords:
- Função glColor3i OpenGL
topic_type:
- apiref
api_name:
- glColor3i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4fe768a2bbc92fba0e2f900ccf15c199f747da1009e288aa83643c30c492e68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360914"
---
# <a name="glcolor3i-function"></a>Função glColor3i

Define a cor atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glColor3i(
   GLint red,
   GLint green,
   GLint blue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Vermelho* 
</dt> <dd>

O novo valor vermelho para a cor atual.

</dd> <dt>

*Verde* 
</dt> <dd>

O novo valor verde para a cor atual.

</dd> <dt>

*Azul* 
</dt> <dd>

O novo valor azul para a cor atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O GL armazena um índice de cor com valor único atual e uma cor RGBA atual de quatro valores. **glcolor** define uma nova cor RGBA de quatro valores. **glcolor** tem duas variantes principais: **glcolor3** e **glcolor4.** **Variantes glcolor3** especificam novos valores vermelhos, verdes e azuis explicitamente e definim o valor alfa atual como 1,0 (intensidade total) implicitamente. **Variantes glcolor4** especificam explicitamente todos os quatro componentes de cores.

**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s,** **glcolor3i** e **glcolor4i** levam três ou quatro inteiros com sinal de byte, curto ou longo como argumentos. Quando v é anexado ao nome, os comandos de cor podem usar um ponteiro para uma matriz de tais valores.

Os valores de cor atuais são armazenados no formato de ponto flutuante, com tamanhos de mantissa e expoentes não especificados. Componentes de cor de inteiro sem sinal, quando especificados, são mapeados linearmente para valores de ponto flutuante, de modo que o maior valor representável mapeia para 1,0 (intensidade total) e 0 é mapeado para 0,0 (intensidade zero). Componentes de cor de inteiro com sinal, quando especificados, são mapeados linearmente para valores de ponto flutuante, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor representável mais negativo é mapeado para -1,0. (Observe que esse mapeamento não converte 0 precisamente em 0,0.) Os valores de ponto flutuante são mapeados diretamente.

Nem valores inteiros com sinal nem de ponto flutuante são fixados ao intervalo \[ 0,1 \] antes que a cor atual seja atualizada. No entanto, os componentes de cor são fixados a esse intervalo antes que sejam interpolados ou gravados em um buffer de cores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindexd.md)
</dt> </dl>

 

 





