---
title: Função AllocCountedString (NapUtil. h)
description: Aloca memória para uma cadeia de caracteres terminada em nulo e a retorna em uma estrutura de conta.
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
ms.openlocfilehash: 4ab2980ce5eefdd7743907bdcc947cdce1c74823
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757769"
---
# <a name="alloccountedstring-function"></a>Função AllocCountedString

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A função **AllocCountedString** aloca memória para uma cadeia de caracteres terminada em nulo e a retorna em uma estrutura de [**conta**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*contado* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para o endereço de uma estrutura de [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) alocada recentemente.

</dd> <dt>

*cadeia de caracteres* \[ no\]
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo que será retornado em *contadostring*.

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

[**FreeCountedString**](freecountedstring-func.md)
</dt> </dl>

 

 





