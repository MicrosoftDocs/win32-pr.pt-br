---
title: função glColor4fv (GL. h)
description: Define a cor atual de uma matriz de valores de cor já existente. | função glColor4fv (GL. h)
ms.assetid: 9052f0a6-5432-49ec-a7f9-a80e3327aeda
keywords:
- função glColor4fv OpenGL
topic_type:
- apiref
api_name:
- glColor4fv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93dd8e80bf600ed72e6095d089889a886388cbd128b6bc377df0928ea57865bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360477"
---
# <a name="glcolor4fv-function"></a>função glColor4fv

Define a cor atual de uma matriz de valores de cor já existente.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glColor4fv(
   const GLfloat *v
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*v* 
</dt> <dd>

Um ponteiro para uma matriz que contém valores vermelho, verde, azul e alfa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O GL armazena um índice de cor de valor único atual e uma cor RGBA atual de quatro valores. **glColor** define uma nova cor RGBA de quatro valores. **glColor** tem duas variantes principais: **glcolor3** e **glcolor4**. as variantes **glcolor3** especificam os novos valores vermelho, verde e azul explicitamente e definem o valor alfa atual como 1,0 (intensidade total) implicitamente. as variantes de **glcolor4** especificam todos os quatro componentes de cores explicitamente.

**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** e **glcolor4i** levam três ou quatro inteiros de bytes assinados, curtos ou longos como argumentos. Quando v é anexado ao nome, os comandos Color podem usar um ponteiro para uma matriz desses valores.

Os valores de cor atuais são armazenados no formato de ponto flutuante, com tamanhos mantissa e expoente não especificados. Os componentes de cor de inteiro não assinados, quando especificados, são mapeados linearmente para valores de ponto flutuante de forma que o maior valor representável seja mapeado para 1,0 (intensidade total) e 0 mapeie para 0,0 (intensidade zero). Os componentes de cor de inteiro assinados, quando especificados, são mapeados linearmente para valores de ponto flutuante, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0. (Observe que esse mapeamento não converte 0 precisamente em 0,0.) Os valores de ponto flutuante são mapeados diretamente.

Os valores inteiros de ponto flutuante e inteiro não assinado são clamped para o intervalo de \[ 0, 1 \] antes da atualização da cor atual. No entanto, os componentes de cor são clamped a esse intervalo antes de serem interpolados ou gravados em um buffer de cores.

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
</dt> <dt>

[**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindexd.md)
</dt> </dl>

 

 





