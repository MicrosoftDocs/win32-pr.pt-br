---
description: Recupera uma cadeia de caracteres ATR do cartão inteligente.
ms.assetid: 2021bd0c-6ef8-4679-be6c-9a9fd33d9fd6
title: 'Método iscard:: get_Atr (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Atr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4f2a5688ee85318003ea366bbce614e8250a131a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748960"
---
# <a name="iscardget_atr-method"></a>Método de @ card:: obter \_ ATR

\[O método **obter \_ ATR** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Get \_ ATR** recupera uma [*cadeia de caracteres ATR*](../secgloss/a-gly.md) do [*cartão inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Atr(
  [out] LPBYTEBUFFER *ppAtr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppAtr* \[ fora\]
</dt> <dd>

Ponteiro para um buffer de bytes na forma de um [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) que conterá a cadeia de caracteres ATR no retorno.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *ppAtr* não é válido.<br/>           |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *ppAtr*.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | A memória para atender à solicitação não está disponível.<br/> |



 

## <a name="remarks"></a>Comentários

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a recuperação da cadeia de caracteres ATR do cartão inteligente.


```C++
// Retrieve the ATR.
// pISCard is a pointer to a previously instantiated ISCard.
// pAtr is a pointer to a previously instantiated IByteBuffer.
hr = pISCard->get_Atr(&pAtr);
if (FAILED(hr))
{
    printf("Failed get_Atr\n");
    // Take other error handling action.
}
// Success, you can now use IByteBuffer::Read to access ATR bytes.
BYTE  byAtr[32];
   long  lBytesRead, i;
   // Read the ATR string into a byte array.
   hr = pAtr->Read(byAtr, 32, &lBytesRead);
   // Use the ATR value. (This example merely displays the bytes.)
   for ( i = 0; i < lBytesRead; i++)
       printf("%c", *(byAtr + i));
   printf("\n");
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

[**IByteBuffer:: ler**](ibytebuffer-read.md)
</dt> </dl>

 

 
