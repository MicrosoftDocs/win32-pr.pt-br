---
title: função glColor3us (GL. h)
description: Define a cor atual. | função glColor3us (GL. h)
ms.assetid: ddce11f4-6bb2-43d0-92b0-11be67c572fe
keywords:
- função glColor3us OpenGL
topic_type:
- apiref
api_name:
- glColor3us
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ce400df429e41ce8642e4a82da6a2f7b7afc2cf551b85c474f02ce9892954ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081866"
---
# <a name="glcolor3us-function"></a>função glColor3us

Define a cor atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glColor3us(
   GLushort red,
   GLushort green,
   GLushort blue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vermelho* 
</dt> <dd>

O novo valor vermelho para a cor atual.

</dd> <dt>

*amarela* 
</dt> <dd>

O novo valor verde para a cor atual.

</dd> <dt>

*azul* 
</dt> <dd>

O novo valor azul para a cor atual.

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

 

 





