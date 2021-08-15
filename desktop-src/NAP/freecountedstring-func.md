---
title: Função FreeCountedString (NapUtil.h)
description: Libera uma estrutura de dados CountedString.
ms.assetid: d080d247-9339-474b-866e-b412e82dd35f
keywords:
- Função FreeCountedString NAP
topic_type:
- apiref
api_name:
- FreeCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff73bc3511f34c8d791c4daf784d57ad12cc343ee9ed5628dd92cc6f4e5fc16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368876"
---
# <a name="freecountedstring-function"></a>Função FreeCountedString

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A **função FreeCountedString** libera uma estrutura [**de dados CountedString.**](/windows/win32/api/naptypes/ns-naptypes-countedstring)

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI VOID WINAPI FreeCountedString(
  _In_ CountedString *countedString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*countedString* \[ Em\]
</dt> <dd>

Um ponteiro para a estrutura [**de dados CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) a ser livre.

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AllocCountedString**](alloccountedstring-func.md)
</dt> </dl>

 

 





