---
description: Executa uma operação de gravação e leitura no objeto de comando de cartão inteligente (unidade de dados do protocolo de aplicativo).
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: 'Método iscard:: Transaction (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749970"
---
# <a name="iscardtransaction-method"></a>Método iscard:: Transaction

\[O método de **transação** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Transaction** executa uma operação de gravação e leitura no objeto de comando de [*cartão inteligente*](../secgloss/s-gly.md) ([*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md)). A cadeia de caracteres de resposta do cartão inteligente para a cadeia de caracteres de comando definida no cartão que foi enviado para o cartão inteligente será acessível depois que essa função retornar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppCmd* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para o objeto de comando do cartão inteligente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | A operação foi concluída com sucesso.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *ppCmd* não é válido.<br/>           |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *ppCmd*.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | A memória para atender à solicitação não está disponível.<br/> |



 

## <a name="remarks"></a>Comentários

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a execução de uma operação de gravação e leitura no objeto de comando do cartão inteligente.


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
}
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

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Detach**](iscard-detach.md)
</dt> <dt>

[**obter \_ ATR**](iscard-get-atr.md)
</dt> <dt>

[**obter \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**obter \_ contexto**](iscard-get-context.md)
</dt> <dt>

[**obter \_ protocolo**](iscard-get-protocol.md)
</dt> <dt>

[**obter \_ status**](iscard-get-status.md)
</dt> <dt>

[**Iscard**](iscard.md)
</dt> <dt>

[**LockSCard**](iscard-lockscard.md)
</dt> <dt>

[**Anexar novamente**](iscard-reattach.md)
</dt> <dt>

[**UnlockSCard**](iscard-unlockscard.md)
</dt> </dl>

 

 
