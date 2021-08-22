---
description: O método Create cria uma nova mídia com propriedades padrão, adiciona-a à coleção no índice especificado e retorna um ponteiro para a interface ITMedia.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: Método ITMediaCollection::Create (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a2b11624b6a22a9bf1bff7b87538d3c7e915892a4ec7b816ee3d6c4d03821d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060864"
---
# <a name="itmediacollectioncreate-method"></a>Método ITMediaCollection::Create

\[As interfaces e controles de Conferência de Telefonia IP de reunião não estão disponíveis para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método Create** cria uma nova mídia com propriedades padrão, adiciona-a à coleção no índice especificado e retorna um ponteiro para a interface [**ITMedia.**](itmedia.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ Em\]
</dt> <dd>

Índice para o novo item. O valor mínimo para o índice é 1 e o valor máximo para o índice é o número atual de itens + 1.

</dd> <dt>

*ppMedia* \[ out\]
</dt> <dd>

Ponteiro para a interface [**ITMedia**](itmedia.md) criada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | O *parâmetro ppMedia* não é um ponteiro válido.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O *parâmetro Index* não é válido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

A maioria das listas C e C++ é baseada em 0, mas esse índice é baseado em 1 para compatibilidade Visual Basic, o que significa que o primeiro item tem um número de índice de 1.

TAPI chama o **método AddRef** na interface [**ITMedia**](itmedia.md) retornada por **ITMediaCollection::Create.** O aplicativo deve chamar **Release** na interface [**ITMedia**](itmedia.md) para liberar recursos associados a ele.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Itmedia**](itmedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




