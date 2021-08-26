---
description: O método ListCards recupera todos os nomes de cartão inteligente que correspondem aos GUIDs (identificadores de interface) especificados, à cadeia de caracteres ATR especificada ou a ambos.
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: 'Método ISCardDatabase:: ListCards (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c34d5d1449b2ef8f34fa87d3a70ecf37787d423a0d5df71ecd15e5f722d112ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014526"
---
# <a name="iscarddatabaselistcards-method"></a>Método ISCardDatabase:: ListCards

\[O método **ListCards** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **ListCards** recupera todos os nomes de cartão inteligente que correspondem aos GUIDs (identificadores de interface) especificados, à [*cadeia de caracteres ATR*](../secgloss/a-gly.md)especificada ou a ambos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAtr* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres ATR de [*cartão inteligente*](../secgloss/s-gly.md) . A cadeia de caracteres ATR deve ser empacotada em um [**IByteBuffer**](ibytebuffer.md).

</dd> <dt>

*pInterfaceGuids* \[ no\]
</dt> <dd>

Ponteiro para um SAFEARRAY de identificadores de interface COM (GUIDs) no formato BSTR.

</dd> <dt>

*LocaleID* \[ no\]
</dt> <dd>

Identificador de localização de idioma.

</dd> <dt>

*ppCardNames* \[ fora\]
</dt> <dd>

Ponteiro para uma SAFEARRAY de BSTRs que contém os nomes dos cartões inteligentes que atenderam aos parâmetros de pesquisa se bem-sucedidos; **NULL** se a operação falhar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

Para recuperar todos os [*leitores*](../secgloss/r-gly.md) ou [*leitor*](../secgloss/r-gly.md)conhecidos, chame [**ListReaders**](iscarddatabase-listreaders.md) ou [**ListReaderGroups**](iscarddatabase-listreadergroups.md) , respectivamente.

Para recuperar o [*serviço primário*](../secgloss/p-gly.md) ou as interfaces de um cartão específico [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) ou [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) , respectivamente.

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardDatabase**](iscarddatabase.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a recuperação de nomes de cartão inteligente que correspondem à cadeia de caracteres ATR especificada.


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
}
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
| IID<br/>                      | IID \_ ISCardDatabase é definido como 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetProviderCardId**](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[**ISCardDatabase**](iscarddatabase.md)
</dt> <dt>

[**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
