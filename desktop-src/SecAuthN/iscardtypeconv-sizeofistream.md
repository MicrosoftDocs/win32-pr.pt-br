---
description: Determina o tamanho, em bytes, da interface COM de IStream.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'Método ISCardTypeConv:: SizeOfIStream (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 603a01dc6cb4727d59a7fb82c3270c08a495f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751525"
---
# <a name="iscardtypeconvsizeofistream-method"></a>Método ISCardTypeConv:: SizeOfIStream

\[O método **SizeOfIStream** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **SizeOfIStream** determina o tamanho, em bytes, da interface com de **IStream** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStrm* \[ no\]
</dt> <dd>

Um ponteiro para a interface com de **IStream** .

</dd> <dt>

*puliSize* \[ fora\]
</dt> <dd>

Um ponteiro para o inteiro grande não assinado que pode conter o valor de sizeof de 64 bits inteiro da interface com de **IStream** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A função teve êxito e *\* puliSize* é o tamanho, em bytes, da interface com de IStream.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>       | Ocorreu uma falha não especificada.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *puliSize* está incorreto.<br/>                                                       |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | O parâmetro *pStrm* está incorreto.<br/>                                                          |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Ocorreu um erro inesperado.<br/>                                                                   |



 

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
| IID<br/>                      | IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valores de retorno do cartão inteligente](authentication-return-values.md)
</dt> </dl>

 

 
