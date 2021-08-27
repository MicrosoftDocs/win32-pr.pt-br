---
description: O método ListCardInterfaces recupera os identificadores (GUIDs) de todas as interfaces com suporte para o cartão inteligente especificado.
ms.assetid: c9dfd17e-f4a9-47d3-974e-66e78bc4b06a
title: 'Método ISCardDatabase:: ListCardInterfaces (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCardInterfaces
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b97569f967c76c985eb05099a21ed10e90456563a871f3e5d9803c6a5875ebdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008104"
---
# <a name="iscarddatabaselistcardinterfaces-method"></a>Método ISCardDatabase:: ListCardInterfaces

\[O método **ListCardInterfaces** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **ListCardInterfaces** recupera os identificadores (GUIDs) de todas as interfaces com suporte para o [*cartão inteligente*](../secgloss/s-gly.md)especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ListCardInterfaces(
  [in]  BSTR        bstrCardName,
  [out] LPSAFEARRAY *ppInterfaceGuids
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrCardName* \[ no\]
</dt> <dd>

Nome do cartão inteligente.

</dd> <dt>

*ppInterfaceGuids* \[ fora\]
</dt> <dd>

Ponteiro para os GUIDs de interface se for bem-sucedido; **Nulo** se a operação falhar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                              |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *ppInterfaceGuids*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                                  |



 

## <a name="remarks"></a>Comentários

Para recuperar o [*provedor de serviços primário*](../secgloss/p-gly.md) do cartão inteligente, chame [**GetProviderCardId**](iscarddatabase-getprovidercardid.md).

Para recuperar todos os [*cartões inteligentes*](../secgloss/s-gly.md), [*leitores*](../secgloss/r-gly.md)e [*grupos*](../secgloss/r-gly.md) de leitores conhecidos, chame [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)e [**ListReaderGroups**](iscarddatabase-listreadergroups.md) , respectivamente.

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardDatabase**](iscarddatabase.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a recuperação dos identificadores das interfaces com suporte para o cartão inteligente especificado.


```C++
BSTR         bstrCard = NULL;
LPSAFEARRAY  pGuids = NULL;
HRESULT      hr;

bstrCard = SysAllocString(L"GemSAFE");
// Call the function for the specified card.
hr = pISCDataBase->ListCardInterfaces(bstrCard,
                                      &pGuids);
if (FAILED(hr))
{
   printf("Failed ListCardInterfaces\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
   // Free BSTR when done.
   if (bstrCard)
       SysFreeString(bstrCard);
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

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
