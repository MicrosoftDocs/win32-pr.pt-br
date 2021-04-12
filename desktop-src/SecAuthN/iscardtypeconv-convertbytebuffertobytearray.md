---
description: Converte um buffer universal de bytes (objeto IStream) em uma matriz de bytes C/C++ típica.
ms.assetid: f5b14096-d848-4de9-a5c3-bb60af9044a2
title: 'Método ISCardTypeConv:: ConvertByteBufferToByteArray (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7eed6758373aebf08863669b5b81909fca1c0840
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170948"
---
# <a name="iscardtypeconvconvertbytebuffertobytearray-method"></a>Método ISCardTypeConv:: ConvertByteBufferToByteArray

\[O método **ConvertByteBufferToByteArray** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **ConvertByteBufferToByteArray** converte um buffer universal de bytes (objeto **IStream** ) em uma matriz de bytes C/C++ típica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConvertByteBufferToByteArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPBYTEARRAY  *ppArray
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbyBuffer* \[ no\]
</dt> <dd>

Ponteiro para o objeto **IStream** a ser convertido.

</dd> <dt>

*ppArray* \[ fora\]
</dt> <dd>

Ponteiro para a matriz de bytes a ser retornada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                                   | Descrição                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memória alocada com êxito.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Há algo errado com um ou mais dos parâmetros passados para a função.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um parâmetro de tipo de ponteiro estava incorreto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória livre suficiente para atender à solicitação.<br/>                                            |



 

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

 

 
