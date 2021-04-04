---
title: função gluLookAt (Glu. h)
description: A função gluLookAt define uma transformação de exibição.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- função gluLookAt OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5866f3c06ef6969c95eeef4b23fff7a4e7852eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824815"
---
# <a name="glulookat-function"></a>função gluLookAt

A função **gluLookAt** define uma transformação de exibição.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*eyex* 
</dt> <dd>

A posição do ponto de olho.

</dd> <dt>

*eyey* 
</dt> <dd>

A posição do ponto de olho.

</dd> <dt>

*eyez* 
</dt> <dd>

A posição do ponto de olho.

</dd> <dt>

*CenterX* 
</dt> <dd>

A posição do ponto de referência.

</dd> <dt>

*CenterY* 
</dt> <dd>

A posição do ponto de referência.

</dd> <dt>

*centerz* 
</dt> <dd>

A posição do ponto de referência.

</dd> <dt>

*upx* 
</dt> <dd>

A direção do vetor para cima.

</dd> <dt>

*upy* 
</dt> <dd>

A direção do vetor para cima.

</dd> <dt>

*upz* 
</dt> <dd>

A direção do vetor para cima.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluLookAt** cria uma matriz de exibição derivada de um ponto de olho, um ponto de referência que indica o centro da cena e um vetor superior. A matriz mapeia o ponto de referência para o eixo z negativo e o ponto de olho para a origem, de modo que, quando você usa uma matriz de projeção típica, o centro da cena é mapeado para o centro do visor. Da mesma forma, a direção descrita pelo vetor de cima projetado no plano de exibição é mapeada para o eixo y positivo para que ele aponte para cima no visor. O vetor acima não deve ser paralelo à linha de visão do olho para o ponto de referência.

A matriz gerada por **gluLookAt** é multiplicada pela matriz atual.

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





