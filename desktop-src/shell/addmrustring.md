---
description: Adiciona uma cadeia de caracteres à parte superior da lista MRU (usada mais recentemente).
title: Função AddMRUStringW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: 0d0d65187105f4ad844b349c6ac60b030c464716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010378"
---
# <a name="addmrustringw-function"></a>Função AddMRUStringW

\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003. Ele pode ser alterado ou indisponível nas versões subsequentes do Windows. \]

Adiciona uma cadeia de caracteres à parte superior da lista MRU (usada mais recentemente).

## <a name="syntax"></a>Sintaxe


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMRU* \[ no\]
</dt> <dd>

Tipo: **identificador**

O identificador da lista MRU.

</dd> <dt>

*szString* \[ no\]
</dt> <dd>

Tipo: **LPCTSTR**

Um ponteiro para os dados. Pode ser uma cadeia de caracteres ou, se a lista MRU tiver sido criada com o sinalizador **\_ binário MRU** , dados binários. No caso de dados binários, a primeira **DWORD** indica seu tamanho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **int**

Retorna um valor não negativo se for bem-sucedido,-1 caso contrário.

## <a name="remarks"></a>Comentários

Essa função não está incluída em um cabeçalho ou biblioteca pública. Ele pode ser acessado por meio de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extraído de comctl32.dll por seu ordinal, que é 401 para **AddMRUStringW**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 5,0 ou posterior)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **AddMRUStringW** (Unicode)<br/>                                                                         |



 

