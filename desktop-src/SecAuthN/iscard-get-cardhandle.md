---
description: Recupera o identificador de um cartão inteligente conectado. Esse método retornará ( \* pHandle) = = NULL se não estiver conectado.
ms.assetid: f03f8f25-b2e4-4fae-b7d2-bb0f1a7cd987
title: 'Método iscard:: get_CardHandle (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_CardHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8a01b7c4531b82c154b6c6e04c1cf0fb5fa2003729e8abf5c0af39470a171bbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482226"
---
# <a name="iscardget_cardhandle-method"></a>Iscard:: obter o \_ método CardHandle

\[O método **Get \_ CardHandle** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Get \_ CardHandle** recupera o identificador de um [*cartão inteligente*](../secgloss/s-gly.md)conectado. Esse método retornará ( \* pHandle) = = **NULL** se não estiver conectado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_CardHandle(
  [out] HSCARD *pHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pHandle* \[ fora\]
</dt> <dd>

Ponteiro para o identificador do cartão no retorno.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operação concluída com sucesso.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *pHandle* não é válido.<br/>  |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Um ponteiro inadequado foi passado em *pHandle*.<br/> |



 

## <a name="remarks"></a>Comentários

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a recuperação da alça do cartão inteligente.


```C++
HSCARD   hSC;
HRESULT  hr;

// Retrieve the card handle.
hr = pISCard->get_CardHandle(&hSC);
if (FAILED(hr))
{
   printf("Failed get_CardHandle\n");
   // Take other error handling action as needed.
}
// Use card handle as needed.
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | \_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**obter \_ ATR**](iscard-get-atr.md)
</dt> <dt>

[**obter \_ contexto**](iscard-get-context.md)
</dt> <dt>

[**obter \_ protocolo**](iscard-get-protocol.md)
</dt> <dt>

[**obter \_ status**](iscard-get-status.md)
</dt> <dt>

[**Iscard**](iscard.md)
</dt> </dl>

 

 
