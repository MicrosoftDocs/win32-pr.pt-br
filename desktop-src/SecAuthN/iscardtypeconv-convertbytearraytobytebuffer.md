---
description: Converte uma matriz de bytes C/C++ típica em um buffer universal de bytes (objeto IStream).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: Método ISCardTypeConv::ConvertByteArrayToByteBuffer (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 5616dc56ac893d6298e12014f3ee31d38bf1c55fb5367f354bf97da704ade0c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013806"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a>Método ISCardTypeConv::ConvertByteArrayToByteBuffer

\[O **método ConvertByteArrayToByteBuffer** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método ConvertByteArrayToByteBuffer** converte uma matriz de bytes C/C++ típica em um buffer universal de bytes (**objeto IStream).**

O buffer de byte criado é um fluxo mapeado sobre um bloco de memória. Para acessar ou gerenciar o buffer, use os métodos fornecidos pela interface **IStream.** Um recurso exclusivo sobre essa implementação de matriz é que, quando você chama o método **IStream::Release,** a memória subjacente será liberada para você.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbyArray* \[ Em\]
</dt> <dd>

Ponteiro para a matriz de bytes a serem convertidos.

</dd> <dt>

*dwArraySize* \[ Em\]
</dt> <dd>

Tamanho da matriz de byte a ser convertida.

</dd> <dt>

*ppbyBuffer* \[ out\]
</dt> <dd>

Ponteiro para o **objeto IStream** a ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                                   | Descrição                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memória alocada com êxito.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Há algo errado com um ou mais dos parâmetros passados para a função.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um parâmetro do tipo de ponteiro estava incorreto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória livre suficiente para atender à solicitação.<br/>                                            |



 

## <a name="remarks"></a>Comentários

A memória alocada é móvel. Use o **método IStream::Release** para liberar a memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardTypeConv é definido como \_ 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valores de retorno de cartão inteligente](authentication-return-values.md)
</dt> </dl>

 

 
