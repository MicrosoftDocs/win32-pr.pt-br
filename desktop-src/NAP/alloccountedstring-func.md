---
title: Função AllocCountedString (NapUtil.h)
description: Aloca memória para uma cadeia de caracteres terminada em nulo e a retorna em uma estrutura CountedString.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- Função AllocCountedString NAP
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef205cf7211f25253a3e6ba0cb7cd84ac37dbdb49848b36e844595d632552331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891736"
---
# <a name="alloccountedstring-function"></a>Função AllocCountedString

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A **função AllocCountedString** aloca memória para uma cadeia de caracteres terminada em nulo e a retorna em uma estrutura [**CountedString.**](/windows/win32/api/naptypes/ns-naptypes-countedstring)

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*countedString* \[ in, out\]
</dt> <dd>

Um ponteiro para o endereço de uma estrutura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) recém-alocada.

</dd> <dt>

*cadeia de caracteres* \[ Em\]
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo que deve ser retornada em *countedString.*

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

[**FreeCountedString**](freecountedstring-func.md)
</dt> </dl>

 

 





