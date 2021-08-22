---
title: função gluQuadricCallback (Glu. h)
description: A função gluQuadricCallback define um retorno de chamada para um objeto Quadric.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- função gluQuadricCallback OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ce32bf041a59f272b18ebe17916963c4e5fd8d208da9d739468c88b9286dfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488786"
---
# <a name="gluquadriccallback-function"></a>função gluQuadricCallback

A função **gluQuadricCallback** define um retorno de chamada para um objeto Quadric.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*qobj* 
</dt> <dd>

O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*Onde* 
</dt> <dd>

O retorno de chamada que está sendo definido. O único valor válido é GLU \_ Error.



| Valor                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <dt>**erro de GLU \_**</dt> </dl> | A função **gluQuadricCallback** é chamada quando um erro é encontrado. Seu único argumento é do tipo **GLenum** e indica o erro específico que ocorreu. As cadeias de caracteres que descrevem esses erros podem ser recuperadas com a chamada [**gluErrorString**](gluerrorstring.md) .<br/> |



 

</dd> <dt>

*fn* 
</dt> <dd>

A função a ser chamada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use **gluQuadricCallback** para definir um novo retorno de chamada a ser usado por um objeto Quadric. Se o retorno de chamada especificado já estiver definido, ele será substituído. Se *FN* for **NULL**, qualquer retorno de chamada existente será apagado.

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

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





