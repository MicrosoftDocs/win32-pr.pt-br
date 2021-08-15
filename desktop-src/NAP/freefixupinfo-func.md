---
title: Função FreeFixupInfo (NapUtil.h)
description: Libera uma estrutura de dados FixupInfo.
ms.assetid: 6bf71ccf-2618-46a3-8a04-9f83a5b7b429
keywords:
- Função FreeFixupInfo NAP
topic_type:
- apiref
api_name:
- FreeFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c869123aadd5310a346dcf8e7a2184ec84f7e40500744cbaf610cbfc54db42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368866"
---
# <a name="freefixupinfo-function"></a>Função FreeFixupInfo

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A **função FreeFixupInfo** libera uma estrutura [**de dados FixupInfo.**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo)

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI VOID WINAPI FreeFixupInfo(
  _In_ FixupInfo *fixupInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fixupInfo* \[ Em\]
</dt> <dd>

Um ponteiro para a estrutura [**de dados FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) a ser livre.

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

[**AllocFixupInfo**](allocfixupinfo-func.md)
</dt> </dl>

 

 





