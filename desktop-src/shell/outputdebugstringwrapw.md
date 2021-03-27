---
description: Envia uma cadeia de caracteres Unicode para o depurador para exibição.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Função OutputDebugStringWrapW (Shlwapip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: e8213aee48a90a816e2968aac115159472ed7b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989018"
---
# <a name="outputdebugstringwrapw-function"></a>Função OutputDebugStringWrapW

\[Essa função está disponível para uso no Windows XP. Ele pode não estar disponível em versões subsequentes. Use [**OutputDebugStringWna**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) em seu lugar.\]

Envia uma cadeia de caracteres Unicode para o depurador para exibição.

> [!Note]  
> **OutputDebugStringWrapW** é um wrapper para a função **OutputDebugStringWna** . Consulte a página [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) para ver mais observações de uso.

 

## <a name="syntax"></a>Sintaxe


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpOutputString* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para a cadeia de caracteres Unicode terminada em nulo a ser exibido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O **OutputDebugStringWrapW** fornece a capacidade de usar cadeias de caracteres Unicode em sistemas operacionais anteriores ao Windows XP. O método preferencial é usar [**OutputDebugStringWna**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) em conjunto com a camada Microsoft para Unicode (MSLU).

**OutputDebugStringWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 115.

Se o aplicativo não tiver um depurador, o depurador do sistema exibirá a cadeia de caracteres. Se o aplicativo não tiver um depurador e o depurador do sistema não estiver ativo, o **OutputDebugStringWrapW** não fará nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shlwapip. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
