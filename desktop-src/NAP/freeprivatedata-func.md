---
title: Função FreePrivateData (NapUtil. h)
description: Libera uma estrutura de dados PrivateData.
ms.assetid: 94b3618e-224f-4801-94f3-2faa1a298ec0
keywords:
- Função FreePrivateData NAP
topic_type:
- apiref
api_name:
- FreePrivateData
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c760a22ef377bd8d198ea3b913c6062e90338218a187cb9dec3af457a8a02493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134612"
---
# <a name="freeprivatedata-function"></a>Função FreePrivateData

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A função **FreePrivateData** libera uma estrutura de dados [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) .

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI VOID WINAPI FreePrivateData(
  _In_ PrivateData *privateData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*privateData* \[ no\]
</dt> <dd>

Um ponteiro para a estrutura de dados [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) para liberar.

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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 





