---
description: Converte uma matriz de bytes definida como SAFEARRAY em um buffer universal de bytes (objeto IStream).
ms.assetid: faa07bb5-cfdb-4181-b86a-f82a9c6b251a
title: Método ISCardTypeConv::ConvertSafeArrayToByteBuffer (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertSafeArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dc7132cbc37a4716adb0dcb192571f9e83597b5aa8b58933962c9366a0c9de2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922432"
---
# <a name="iscardtypeconvconvertsafearraytobytebuffer-method"></a>Método ISCardTypeConv::ConvertSafeArrayToByteBuffer

\[O **método ConvertSafeArrayToByteBuffer** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método ConvertSafeArrayToByteBuffer** converte uma matriz de bytes definida como SAFEARRAY em um buffer universal de bytes (**objeto IStream).**

O buffer de byte criado é um fluxo mapeado sobre um bloco de memória. Para acessar ou gerenciar o buffer, use os métodos fornecidos pela interface **IStream.** Um recurso exclusivo sobre essa implementação de matriz é que, quando você chama o método **IStream::Release,** a memória subjacente será liberada para você.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConvertSafeArrayToByteBuffer(
  [in]  LPSAFEARRAY  pbyArray,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbyArray* \[ Em\]
</dt> <dd>

Ponteiro para SAFEARRAY a ser convertido.

</dd> <dt>

*ppbyBuff* \[ out\]
</dt> <dd>

Ponteiro para o **objeto IStream** a ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memória alocada com êxito.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Há algo errado com um ou mais dos parâmetros passados para a função.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um parâmetro do tipo de ponteiro estava incorreto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória livre suficiente para atender à solicitação.<br/>                                            |



 

## <a name="remarks"></a>Comentários

A memória alocada é movêvel. Use o **método IStream::Release** para liberar a memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardTypeConv é definido como \_ 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valores de retorno de cartão inteligente](authentication-return-values.md)
</dt> </dl>

 

 
