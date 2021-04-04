---
title: Função AllocFixupInfo (NapUtil. h)
description: Aloca memória para uma estrutura FixupInfo do tamanho especificado.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- Função AllocFixupInfo NAP
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dffda7e5e44302173ac06e460414455eb19c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824214"
---
# <a name="allocfixupinfo-function"></a>Função AllocFixupInfo

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A função **AllocFixupInfo** aloca memória para uma estrutura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) do tamanho especificado.

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fixupInfo* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para o endereço de uma estrutura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) alocada recentemente.

</dd> <dt>

*countResultCodes* \[ no\]
</dt> <dd>

O número de códigos de resultado a serem alocados ao *fixupInfo*.

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

[**FreeFixupInfo**](freefixupinfo-func.md)
</dt> </dl>

 

 





