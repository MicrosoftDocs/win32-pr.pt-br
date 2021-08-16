---
description: O método Create cria um novo componente ITTime.
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: Método ITTimeCollection::Create (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a65949d0584f6ed41d3e1611c790b6b94dfa88a4e11ba18818974af5d38cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762368"
---
# <a name="ittimecollectioncreate-method"></a>Método ITTimeCollection::Create

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método Create** cria um novo componente [**ITTime.**](ittime.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ Em\]
</dt> <dd>

Índice do item a ser criado. (A matriz de índice é baseada em um.)

</dd> <dt>

*ppTime* \[ out\]
</dt> <dd>

Ponteiro para o componente b criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | O *parâmetro ppTime* não é um ponteiro válido.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro Index* não é válido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

TAPI chama o **método AddRef** na interface [**ITTime**](ittime.md) retornada por **ITTimeCollection::Create**. O aplicativo deve chamar **Release** na interface v para liberar recursos associados a ele.

Essa função pode enviar dados pela transmissão em formato não criptografado; portanto, alguém que está escutando na rede pode conseguir ler os dados. O risco de segurança de enviar os dados em texto não claro deve ser considerado antes de usar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

 




