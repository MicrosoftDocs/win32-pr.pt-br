---
title: Função FreeConnections (NapUtil. h)
description: Libera uma estrutura de dados de conexões.
ms.assetid: bb339d71-f8e3-48d8-834d-8b957e0cb5ec
keywords:
- Função FreeConnections NAP
topic_type:
- apiref
api_name:
- FreeConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f840d02572af3e6382a06a1873573fc7a30420e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294763"
---
# <a name="freeconnections-function"></a>Função FreeConnections

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A função **FreeConnections** libera uma estrutura de dados de [**conexões**](connections-struct.md) .

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI VOID WINAPI FreeConnections(
  _In_ Connections *connections
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*conexões* \[ do no\]
</dt> <dd>

Um ponteiro para a estrutura de [**conexões**](connections-struct.md) para gratuito.

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AllocConnections**](allocconnections-func.md)
</dt> </dl>

 

 





