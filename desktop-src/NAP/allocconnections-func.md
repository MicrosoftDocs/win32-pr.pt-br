---
title: Função AllocConnections (NapUtil. h)
description: Aloca memória para um número especificado de estruturas de conexões.
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- Função AllocConnections NAP
topic_type:
- apiref
api_name:
- AllocConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e29521d2fea6eec3765a3a34210b896f1baa4db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645249"
---
# <a name="allocconnections-function"></a>Função AllocConnections

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A função **AllocConnections** aloca memória para um número especificado de estruturas de [**conexões**](connections-struct.md) .

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*conexões* \[ do entrada, saída\]
</dt> <dd>

Um ponteiro para uma matriz de estruturas de [**conexões**](connections-struct.md) alocadas recentemente.

</dd> <dt>

*connectionsCount* \[ no\]
</dt> <dd>

O número de estruturas para alocar a *conexões*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor



| Código de retorno                                                                                   | Descrição                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | A operação foi concluída com êxito.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um argumento inválido foi passado.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | O sistema está sem memória virtual. Esta operação falhou.<br/> |



 

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

[**FreeConnections**](freeconnections-func.md)
</dt> </dl>

 

 





