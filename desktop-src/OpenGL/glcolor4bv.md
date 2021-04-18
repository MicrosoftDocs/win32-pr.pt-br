---
title: função glColor4bv (GL. h)
description: Define a cor atual de uma matriz de valores de cor já existente. | função glColor4bv (GL. h)
ms.assetid: 97070501-3718-4946-acc1-1f9f07fa156c
keywords:
- função glColor4bv OpenGL
topic_type:
- apiref
api_name:
- glColor4bv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2691a357f3669e83163eeb9cda04fd26cd89a918
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105780856"
---
# <a name="glcolor4bv-function"></a>função glColor4bv

Define a cor atual de uma matriz de valores de cor já existente.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glColor4bv(
   const GLbyte *v
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*l* 
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

 

 





