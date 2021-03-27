---
description: Enumera o conteúdo da lista MRU (usada mais recentemente). Opcionalmente, recupera um item da enumeração.
title: Função EnumMRUListW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 6b6e9588588e44a2c3b40f6ac012b11f21c875e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829704"
---
# <a name="enummrulistw-function"></a>Função EnumMRUListW

\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003. Ele pode ser alterado ou indisponível nas versões subsequentes do Windows. \]

Enumera o conteúdo da lista MRU (usada mais recentemente). Opcionalmente, recupera um item da enumeração.

## <a name="syntax"></a>Sintaxe


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMRU* \[ no\]
</dt> <dd>

Tipo: **identificador**

O identificador da lista MRU, obtido quando a lista foi criada.

</dd> <dt>

*nItem* \[ no\]
</dt> <dd>

Tipo: **int**

O item a ser retornado. Se esse valor for menor que 0, a função retornará o número de itens na lista MRU.

</dd> <dt>

*lpData* \[ fora\]
</dt> <dd>

Tipo: **void \** _

Um ponteiro para um buffer que recebe o item solicitado em _nItem *. Se *nItem* for menor que 0, o conteúdo desse buffer não será alterado.

</dd> <dt>

*uLen* \[ no\]
</dt> <dd>

Tipo: **uint**

O tamanho do buffer, incluindo o caractere nulo de terminação. Se a lista MRU foi criada com o **sinalizador \_ binário MRU** , esse é o tamanho em bytes. Caso contrário, é o tamanho em caracteres.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **int**

Retorna um dos valores a seguir.

-   Retorna o número de itens na enumeração, se *nItem* for menor que 0.
-   Retornará-1 se ocorrer um erro.
-   Caso contrário, retorna o tamanho da cadeia de caracteres retornada em *lpData*, incluindo o caractere nulo de terminação. Se a lista MRU foi criada com o **sinalizador \_ binário MRU** , esse é o tamanho em bytes. Caso contrário, é o tamanho em caracteres.

## <a name="remarks"></a>Comentários

Essa função não está incluída em um cabeçalho ou biblioteca pública. Ele pode ser acessado por meio de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extraído de comctl32.dll por seu ordinal, que é 403 para **EnumMRUListW**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 5,0 ou posterior)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **EnumMRUListW** (Unicode)<br/>                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CreateMRUListW**](createmrulist.md)
</dt> <dt>

[**MRUINFO**](mruinfo.md)
</dt> </dl>

 

 
