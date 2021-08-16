---
description: Envia uma cadeia de caracteres Unicode para o depurador para exibição.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: Função OutputDebugStringWrapW (Shlwapip.h)
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
ms.openlocfilehash: cce8754b01ddf156951964b7189b4a7189759c52cdcd08e08091ca62b2e950bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858785"
---
# <a name="outputdebugstringwrapw-function"></a>Função OutputDebugStringWrapW

\[Essa função está disponível para uso no Windows XP. Ele pode não estar disponível em versões subsequentes. Use [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) em seu lugar.\]

Envia uma cadeia de caracteres Unicode para o depurador para exibição.

> [!Note]  
> **OutputDebugStringWrapW** é um wrapper para a **função OutputDebugStringW.** Consulte a [**página OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) para ver mais observações de uso.

 

## <a name="syntax"></a>Sintaxe


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpOutputString* \[ Em\]
</dt> <dd>

Tipo: **LPCWSTR**

Um ponteiro para a cadeia de caracteres Unicode terminada em nulo a ser exibida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

**OutputDebugStringWrapW fornece** a capacidade de usar cadeias de caracteres Unicode em sistemas operacionais antes Windows XP. O método preferencial é usar [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) em conjunto com o MSLU (Camada da Microsoft para Unicode).

**OutputDebugStringWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 115.

Se o aplicativo não tiver nenhum depurador, o depurador do sistema exibirá a cadeia de caracteres. Se o aplicativo não tiver nenhum depurador e o depurador do sistema não estiver ativo, **OutputDebugStringWrapW** não faz nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shlwapip.h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Outputdebugstring**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
