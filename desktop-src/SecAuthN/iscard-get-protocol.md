---
description: Recupera o identificador do protocolo atualmente em uso no cartão inteligente.
ms.assetid: 68c75e98-da5c-4e3e-9836-369941751fb0
title: 'Método iscard:: get_Protocol (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Protocol
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb58f890da85e3348ede6af70a006f98daac38a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297259"
---
# <a name="iscardget_protocol-method"></a>Método de protocolo iscard:: get \_

\[O método **Get \_ Protocol** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Get \_ Protocol** recupera o identificador do protocolo atualmente em uso no [*cartão inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Protocol(
  [out] SCARD_PROTOCOLS *pProtocol
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pProtocol* \[ fora\]
</dt> <dd>

Ponteiro para o identificador de protocolo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operação concluída com sucesso.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *pProtocol* não é válido.<br/>  |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Um ponteiro inadequado foi passado em *pProtocol*.<br/> |



 

## <a name="remarks"></a>Comentários

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a recuperação do identificador do protocolo atualmente em uso no cartão inteligente.


```C++
SCARD_PROTOCOLS   scProtocol;
HRESULT           hr;

// Retrieve the protocol.
hr = pISCard->get_Protocol(&scProtocol);
if (FAILED(hr))
{
   printf("Failed get_Protocol\n");
   // Take other error handling action as needed.
}
// Use the retrieved protocol. (This example merely displays it.)
switch (scProtocol)
{
    case T0:
        printf("T0 protocol\n");
        break;
    case T1:
        printf("T1 protocol\n");
        break;
    default:
        printf("Other protocol\n");
        break;
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

[**obter \_ ATR**](iscard-get-atr.md)
</dt> <dt>

[**obter \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**obter \_ contexto**](iscard-get-context.md)
</dt> <dt>

[**obter \_ status**](iscard-get-status.md)
</dt> <dt>

[**Iscard**](iscard.md)
</dt> </dl>

 

 
