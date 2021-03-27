---
description: Converte caracteres minúsculos em um buffer em caracteres maiúsculos.
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
ms.openlocfilehash: dacc5e7609ca7f91bf7c66651d7ba9bdd11ab688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501437"
---
# <a name="charupperbuffwrapw-function"></a>Função CharUpperBuffWrapW

\[O **CharUpperBuffWrapW** está disponível para uso no Windows XP. Ele pode não estar disponível em versões subsequentes. Você deve usar [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) em seu lugar.\]

Converte caracteres minúsculos em um buffer em caracteres maiúsculos. A função converte os caracteres em vigor.

> [!Note]  
> **CharUpperBuffWrapW** é um wrapper para a função **CharUpperBuffW** . Consulte a página [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) para ver mais observações de uso.

 

## <a name="syntax"></a>Sintaxe


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PCH* \[ no\]
</dt> <dd>

Tipo: **LPWSTR**

Um ponteiro para um buffer que contém um ou mais caracteres Unicode a serem processados.

</dd> <dt>

*cchLength* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Especifica o tamanho, em caracteres, do buffer apontado por *PCH*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **DWORD**

O número de caracteres processados.

## <a name="remarks"></a>Comentários

O método preferencial é usar [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) em conjunto com a camada Microsoft para Unicode (MSLU).

**CharUpperBuffWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 44.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
