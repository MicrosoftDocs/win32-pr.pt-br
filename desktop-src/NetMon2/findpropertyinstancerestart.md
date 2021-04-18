---
description: Localiza a próxima instância da propriedade especificada pelo parâmetro hProperty.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: Função FindPropertyInstanceRestart (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d1e731bb00b28bb62862dd18fbd6031fa973fe38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778708"
---
# <a name="findpropertyinstancerestart-function"></a>Função FindPropertyInstanceRestart

A função **FindPropertyInstanceRestart** localiza a próxima instância da propriedade especificada pelo parâmetro *hProperty* .

## <a name="syntax"></a>Sintaxe


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Um identificador para o quadro. O identificador de quadro pode ser recuperado por uma chamada para a função [GetFrame](getframe.md) .

</dd> <dt>

*hProperty* \[ no\]
</dt> <dd>

Um identificador para a propriedade a ser localizada. O identificador de propriedade pode ser recuperado por uma chamada para a função [GetProperty](getproperty.md) .

</dd> <dt>

*lpRestartKey* \[ no\]
</dt> <dd>

Um ponteiro para a instância de propriedade usado como o ponto de partida da pesquisa. Se o parâmetro *lpRestartKey* for definido como **NULL**, a pesquisa começará no início do quadro ou no final do quadro, dependendo do valor do parâmetro *DirForward* .

Se *lpRestartKey* apontar para **NULL**, a pesquisa começará no início do quadro se *DirForward* for **true** ou no final do quadro se o parâmetro for **false**.

</dd> <dt>

*DirForward* \[ no\]
</dt> <dd>

Um indicador da direção da pesquisa. Se o valor for **true**, a pesquisa será movida do local atual para o fim do quadro. Se o valor for **false**, a pesquisa se moverá do local atual para o início do quadro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será o próximo **LPPROPERTYINST** válido.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **FindPropertyInstanceRestart** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[GetFrame](getframe.md)
</dt> <dt>

[GetProperty](getproperty.md)
</dt> </dl>

 

 




