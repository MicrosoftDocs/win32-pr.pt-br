---
description: Converte caracteres minúsculos em um buffer em caracteres maiúsculas.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: Função CharUpperBuffWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 288a119586e9f2e58172daaba33a8b9f27c791aa0005b5349f47cb0b2670a631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861551"
---
# <a name="charupperbuffwrapw-function"></a>Função CharUpperBuffWrapW

\[**CharUpperBuffWrapW** está disponível para uso no Windows XP. Ele pode não estar disponível em versões subsequentes. Você deve usar [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) em seu lugar.\]

Converte caracteres minúsculos em um buffer em caracteres maiúsculas. A função converte os caracteres no local.

> [!Note]  
> **CharUpperBuffWrapW** é um wrapper para a **função CharUpperBuffW.** Consulte a [**página CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) para ver mais observações de uso.

 

## <a name="syntax"></a>Sintaxe


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pch* \[ Em\]
</dt> <dd>

Tipo: **LPWSTR**

Um ponteiro para um buffer que contém um ou mais caracteres Unicode a processar.

</dd> <dt>

*cchLength* \[ Em\]
</dt> <dd>

Tipo: **DWORD**

Especifica o tamanho, em caracteres, do buffer apontado por *pch*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **DWORD**

O número de caracteres processados.

## <a name="remarks"></a>Comentários

O método preferencial é usar [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) em conjunto com o MSLU (Camada da Microsoft para Unicode).

**CharUpperBuffWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 44.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
