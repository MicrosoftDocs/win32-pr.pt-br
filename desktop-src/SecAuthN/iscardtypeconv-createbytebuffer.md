---
description: Cria um buffer universal de bytes mapeados em um objeto IStream (IByteBuffer).
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: 'Método ISCardTypeConv:: CreateByteBuffer (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e95ab8989027cb79dfd48720b08d27042c7bd8f9252d1438152dafbae017d762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922405"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a>Método ISCardTypeConv:: CreateByteBuffer

\[O método **CreateByteBuffer** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **CreateByteBuffer** cria um buffer universal de bytes mapeados em um objeto **IStream** ([**IByteBuffer**](ibytebuffer.md)).

O buffer de bytes criado é um fluxo mapeado em um bloco de memória. Para acessar ou gerenciar o buffer, use os métodos fornecidos pela interface **IStream** . Um recurso exclusivo sobre essa implementação de matriz é que quando você chama o método **IStream:: Release** , a memória subjacente será liberada para você.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwAllocSize* \[ no\]
</dt> <dd>

Tamanho em bytes da memória a ser alocada para a matriz.

</dd> <dt>

*ppbyBuff* \[ fora\]
</dt> <dd>

Ponteiro para o objeto IStream a ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Os possíveis valores de retorno são os seguintes:



| Código de retorno                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memória alocada com êxito.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Há algo errado com um ou mais dos parâmetros passados para a função.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória livre suficiente para atender à solicitação.<br/>                                            |



 

## <a name="remarks"></a>Comentários

A memória alocada é móvel. Use o método **IStream:: Release** para liberar a memória.

Para criar uma matriz de bytes C/C++ típica, chame [**CreateByteArray**](iscardtypeconv-createbytearray.md).

Para criar um SAFEARRAY de automação de caracteres não assinados (bytes), chame [**createsafearray**](iscardtypeconv-createsafearray.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
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
</dt> <dt>

[**CreateByteArray**](iscardtypeconv-createbytearray.md)
</dt> <dt>

[**Createsafearray**](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
