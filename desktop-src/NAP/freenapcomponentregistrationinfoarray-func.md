---
title: Função FreeNapComponentRegistrationInfoArray (NapUtil.h)
description: Libera um número especificado de estruturas de dados NapComponentRegistrationInfo de uma matriz.
ms.assetid: 6fcb1394-04dd-4d8a-87f7-6b69b6ef29ff
keywords:
- Função NAP FreeNapComponentRegistrationInfoArray
topic_type:
- apiref
api_name:
- FreeNapComponentRegistrationInfoArray
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d9d1aba35e7bf1ef332231836bd986b881f0e2dc995bc430075dfadf7bd482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940494"
---
# <a name="freenapcomponentregistrationinfoarray-function"></a>Função FreeNapComponentRegistrationInfoArray

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A **função FreeNapComponentRegistrationInfoArray** libera um número especificado de estruturas de dados [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) de uma matriz.

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI VOID WINAPI FreeNapComponentRegistrationInfoArray(
  _In_ UINT16                       count,
  _In_ NapComponentRegistrationInfo **info
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*count* \[ Em\]
</dt> <dd>

O número de [**estruturas NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) em *informações* a liberar.

</dd> <dt>

*informações* \[ Em\]
</dt> <dd>

Um ponteiro para uma matriz de [**estruturas de dados NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) a serem liberadas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Todas as interfaces COM com suporte pelo sistema NAP usam regras de gerenciamento de memória COM padrão e alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

-   **Em,** os parâmetros são alocados e liberados pelo chamador.
-   **Os** parâmetros out são alocados pelo chamador e liberados pelo chamador usando **CoTaskMem.**
-   **Os parâmetros** de saída são alocados pelo chamador, liberados e realocados pelo chamador e, por fim, liberados pelo chamador, usando **CoTaskMem.**

Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 





