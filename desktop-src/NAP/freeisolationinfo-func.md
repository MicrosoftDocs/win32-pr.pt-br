---
title: Função FreeIsolationInfo (NapUtil. h)
description: Libera uma estrutura de dados IsolationInfo.
ms.assetid: 639cfa74-0823-4a19-9cbe-dd6f0a38e7eb
keywords:
- Função FreeIsolationInfo NAP
topic_type:
- apiref
api_name:
- FreeIsolationInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ed154d35b32edab0f1a68d84f78c10cfd1cfe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766371"
---
# <a name="freeisolationinfo-function"></a>Função FreeIsolationInfo

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A função **FreeIsolationInfo** libera uma estrutura de dados [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) .

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI VOID WINAPI FreeIsolationInfo(
  _In_ IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*isolationInfo* \[ no\]
</dt> <dd>

Um ponteiro para a estrutura de dados [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) para liberar.

</dd> </dl>

## <a name="remarks"></a>Comentários

Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e os alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

-   **Em** parâmetros são alocados e liberados pelo chamador.
-   Os parâmetros de **saída** são alocados pelo receptor e liberados pelo chamador usando **CoTaskMem**.
-   Os parâmetros **in/out** são alocados pelo chamador, liberados e realocados pelo receptor e, por fim, liberados pelo chamador, usando **CoTaskMem**.

Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 





