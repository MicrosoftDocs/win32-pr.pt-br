---
title: Função AllocFixupInfo (NapUtil.h)
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
ms.openlocfilehash: 95ce329a433439716700b6ffc990d446c5d22faab91fa256f6abc0c73734327d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803486"
---
# <a name="allocfixupinfo-function"></a>Função AllocFixupInfo

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A **função AllocFixupInfo** aloca memória para uma [**estrutura FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) do tamanho especificado.

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fixupInfo* \[ in, out\]
</dt> <dd>

Um ponteiro para o endereço de uma estrutura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) recém-alocada.

</dd> <dt>

*countResultCodes* \[ Em\]
</dt> <dd>

O número de códigos de resultado a alocar para *fixupInfo.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado



| Código de retorno                                                                                   | Descrição                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | A operação foi concluída com êxito.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um argumento inválido foi passado.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | O sistema está sem memória virtual. Esta operação falhou.<br/> |



 

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

[**FreeFixupInfo**](freefixupinfo-func.md)
</dt> </dl>

 

 





