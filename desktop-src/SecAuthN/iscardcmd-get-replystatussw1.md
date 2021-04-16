---
description: Recupera o byte de status de APDUs SW1 de resposta.
ms.assetid: 5f74d0c9-cf82-4694-bca6-a2655e717a1f
title: 'Método ISCardCmd:: get_ReplyStatusSW1 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92bcf490a3cb1fc533bcf9a1046642d3c3e55b59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501755"
---
# <a name="iscardcmdget_replystatussw1-method"></a>Método ISCardCmd:: get \_ ReplyStatusSW1

\[O método **Get \_ ReplyStatusSW1** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Get \_ ReplyStatusSW1** recupera o byte de status de APDUs SW1 de [*resposta*](../secgloss/r-gly.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ReplyStatusSW1(
  [out] LPBYTE pbySW1
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbySW1* \[ fora\]
</dt> <dd>

Ponteiro para o byte que contém o valor do byte de SW1 no retorno.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pbySW1* não é válido.<br/>  |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *pbySW1*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                        |



 

## <a name="remarks"></a>Comentários

O byte de status de SW1 [*do APDU de resposta*](../secgloss/r-gly.md) é somente leitura.

Para recuperar o byte de status do SW2 do APDU de resposta, chame [**Get \_ ReplyStatusSW2**](iscardcmd-get-replystatussw2.md).

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como recuperar o byte de status de SW1 da [*resposta APDU*](../secgloss/r-gly.md). O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .


```C++
BYTE     bySW1;
HRESULT  hr;

// Retrieve the reply status SW1 byte.
hr = pISCardCmd->get_ReplyStatusSW1(&bySW1);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW1\n");
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
| parâmetro<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**obter \_ ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)
</dt> <dt>

[**obter \_ ReplyStatus**](iscardcmd-get-replystatus.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
