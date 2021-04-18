---
description: O método ListReaders recupera os nomes dos leitores de cartão inteligente registrados no banco de dados do cartão inteligente.
ms.assetid: e1ca85a1-9206-4c09-ba0f-10b60e472dfb
title: 'Método ISCardDatabase:: ListReaders (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaders
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dcd78066a95c69b75d5089ba1683e5c937cb7414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752015"
---
# <a name="iscarddatabaselistreaders-method"></a>Método ISCardDatabase:: ListReaders

\[O método **ListReaders** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **ListReaders** recupera os nomes dos [*leitores*](../secgloss/r-gly.md) de cartão inteligente registrados no banco de [*dados do cartão inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ListReaders(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaders
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LocaleID* \[ no\]
</dt> <dd>

ID da localização do idioma.

</dd> <dt>

*ppReaders* \[ fora\]
</dt> <dd>

Ponteiro para um SAFEARRAY de BSTRs que contém os nomes dos leitores de cartão inteligente, se for bem-sucedido; **NULL** se a operação falhar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                       |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *ppReaders*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                           |



 

## <a name="remarks"></a>Comentários

Para recuperar todos os [*cartões inteligentes*](../secgloss/s-gly.md) ou [*grupos de leitores*](../secgloss/r-gly.md)conhecidos, chame [**ListCards**](iscarddatabase-listcards.md) ou [**ListReaderGroups**](iscarddatabase-listreadergroups.md) , respectivamente.

Para recuperar o [*provedor de serviços primário*](../secgloss/p-gly.md) ou as interfaces de um cartão específico [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) ou [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) , respectivamente.

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardDatabase**](iscarddatabase.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a recuperação dos nomes dos leitores de cartão inteligente registrados no banco de dados do cartão inteligente.


```C++
LPSAFEARRAY pReaders = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaders(0x0409,  // English (US)
                               &pReaders);
if (FAILED(hr))
{
   printf("Failed ListReaders\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
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
| IID<br/>                      | IID \_ ISCardDatabase é definido como 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetProviderCardId**](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[**ISCardDatabase**](iscarddatabase.md)
</dt> <dt>

[**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> </dl>

 

 
