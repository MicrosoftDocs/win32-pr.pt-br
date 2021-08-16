---
description: Adiciona uma cadeia de caracteres à parte superior da lista de MRU (usados mais recentemente).
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
ms.openlocfilehash: 4ac72c44b670466f10cd708b81b1a84f93a349afcb0d81473ed5e6578c20617a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861588"
---
# <a name="addmrustringw-function"></a>Função AddMRUStringW

\[Essa função está disponível por meio Windows XP com Service Pack 2 (SP2) e Windows Server 2003. Ele pode ser alterado ou não disponível nas versões subsequentes do Windows. \]

Adiciona uma cadeia de caracteres à parte superior da lista de MRU (usados mais recentemente).

## <a name="syntax"></a>Sintaxe


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMRU* \[ Em\]
</dt> <dd>

Tipo: **HANDLE**

O alça da lista mru.

</dd> <dt>

*szString* \[ Em\]
</dt> <dd>

Tipo: **LPCTSTR**

Um ponteiro para os dados. Isso pode ser uma cadeia de caracteres ou, se a lista mru foi criada com o sinalizador **\_ BINARY do MRU,** dados binários. No caso de dados binários, a primeira **DWORD** indica seu tamanho.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **int**

Retornará um valor não negativo se for bem-sucedido; caso contrário, -1.

## <a name="remarks"></a>Comentários

Essa função não está incluída em um header ou biblioteca público. Ele pode ser acessado por [**meio de GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extraído do comctl32.dll por seu ordinal, que é 401 para **AddMRUStringW.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 5.0 ou posterior)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **AddMRUStringW** (Unicode)<br/>                                                                         |



 

