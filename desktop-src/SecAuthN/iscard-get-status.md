---
description: Recupera o estado atual do cartão inteligente.
ms.assetid: 0e6e4a8f-ecad-4a82-8804-aaf58f13f7ca
title: Método ISCard::get_Status (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Status
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 695fc21a651522321c1213cb3e8c87fa156710014e7ab8114b94e0d50efe00b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015596"
---
# <a name="iscardget_status-method"></a>Método ISCard::get \_ Status

\[O **método \_ get Status** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método \_ get Status** recupera o estado [*atual*](../secgloss/s-gly.md) do [*cartão inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Status(
  [out] SCARD_STATES *pStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStatus* \[ out\]
</dt> <dd>

Ponteiro para a variável de estado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operação concluída com sucesso.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O *parâmetro pStatus* não é válido.<br/>  |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>    | Um ponteiro ruim foi passado em *pStatus*.<br/> |



 

## <a name="remarks"></a>Comentários

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir a solicitação. Para obter mais informações, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a recuperação do estado atual do cartão inteligente.


```C++
SCARD_STATES    scState;
HRESULT         hr;

// Determine the current state of the smart card.
hr = pISCard->get_Status(&scState);
if (FAILED(hr))
{
   printf("Failed get_Status\n");
   exit(1);  // Or other error handling action.
}
// Use the retrieved value. (This example merely displays it.)
switch (scState)
{
    case ABSENT:
        printf("Absent state\n");
        break;
    case PRESENT:
        printf("Present state\n");
        break;
    case SWALLOWED:
        printf("Swallowed state\n");
        break;
    case POWERED:
        printf("Powered state\n");
        break;
    case NEGOTIABLEMODE:
        printf("Negotiable mode state\n");
        break;
    case SPECIFICMODE:
        printf("Specific mode state\n");
        break;
    default:
        printf("Unexpected state\n");
        break;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCard é definido como \_ 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**get \_ Atr**](iscard-get-atr.md)
</dt> <dt>

[**get \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**obter \_ contexto**](iscard-get-context.md)
</dt> <dt>

[**obter \_ protocolo**](iscard-get-protocol.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> </dl>

 

 
