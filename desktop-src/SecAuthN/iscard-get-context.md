---
description: Recupera o identificador de contexto atual do Resource Manager. Esse método retornará ( \* pContext) = = NULL se nenhum contexto tiver sido estabelecido.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: 'Método iscard:: get_Context (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8b5aba075d755b644a78cca23a827a70966f4ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829755"
---
# <a name="iscardget_context-method"></a>Método de contexto iscard:: get \_

\[O método de **\_ contexto Get** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método de **\_ contexto Get** recupera o identificador de contexto atual do [*Resource Manager*](../secgloss/r-gly.md) . Esse método retornará ( \* *pContext*) = = **NULL** se nenhum contexto tiver sido estabelecido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContext* \[ fora\]
</dt> <dd>

Ponteiro para o identificador de contexto no retorno.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operação concluída com sucesso.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *pContext* não é válido.<br/>  |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Um ponteiro inadequado foi passado em *pContext*.<br/> |



 

## <a name="remarks"></a>Comentários

O contexto do Gerenciador de recursos é definido chamando a função de [*cartão inteligente*](../secgloss/s-gly.md) [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a recuperação do identificador de [*contexto do Resource Manager*](../secgloss/r-gly.md) atual.


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | \_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**obter \_ ATR**](iscard-get-atr.md)
</dt> <dt>

[**obter \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**obter \_ protocolo**](iscard-get-protocol.md)
</dt> <dt>

[**obter \_ status**](iscard-get-status.md)
</dt> <dt>

[**Iscard**](iscard.md)
</dt> <dt>

[**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
