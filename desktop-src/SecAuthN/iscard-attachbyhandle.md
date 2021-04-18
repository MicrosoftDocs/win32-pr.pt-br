---
description: Anexa o objeto iscard a um identificador de cartão inteligente aberto e configurado.
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: 'Método iscard:: AttachByHandle (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e72ce215b373ef8bd48921f796083e9bc5e801be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749686"
---
# <a name="iscardattachbyhandle-method"></a>Método iscard:: AttachByHandle

\[O método **AttachByHandle** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **AttachByHandle** anexa o objeto [**iscard**](iscard.md) a um identificador de [*cartão inteligente*](../secgloss/s-gly.md) aberto e configurado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hCard* \[ no\]
</dt> <dd>

Um identificador para uma conexão aberta com um cartão inteligente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operação concluída com sucesso.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *hCard* não é válido.<br/> |



 

## <a name="remarks"></a>Comentários

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

Quando terminar de usar o identificador, libere o anexo chamando o método [**iscard::D Etach**](iscard-detach.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a anexação a um identificador de cartão inteligente.


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
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

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Detach**](iscard-detach.md)
</dt> <dt>

[**obter \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**Iscard**](iscard.md)
</dt> <dt>

[**Anexar novamente**](iscard-reattach.md)
</dt> </dl>

 

 
