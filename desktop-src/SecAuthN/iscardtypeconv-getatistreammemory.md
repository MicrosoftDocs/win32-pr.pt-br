---
description: Adquire um ponteiro de byte para o bloco de memória HGLOBAL que é gerenciado pela interface COM do IStream.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: Método ISCardTypeConv::GetAtIStreamMemory (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6520b9af0cf8f322045dfbe92ffc66ef624eadfa7b1beef0f528c6b299d1c2bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922395"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a>Método ISCardTypeConv::GetAtIStreamMemory

\[O **método GetAtIStreamMemory** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método GetAtIStreamMemory** adquire um ponteiro de byte para o bloco de memória HGLOBAL gerenciado pela interface COM **IStream.**

Essa é uma maneira de obter a memória no **IStream** sem precisar obter o valor sizeof do bloco de memória em bytes e ler os bytes em uma matriz de bytes temporária usando a interface **IStream.**

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStrm* \[ Em\]
</dt> <dd>

Um ponteiro para a interface COM **do IStream** que gerencia o bloco de memória HGLOBAL.

</dd> <dt>

*ppMem* \[ out\]
</dt> <dd>

Um ponteiro para o primeiro byte do bloco de memória HGLOBAL, se bem-sucedido; else, **NULL** se a operação falhar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memória alocada com êxito.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Há algo errado com um ou mais dos parâmetros passados para a função.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um parâmetro do tipo de ponteiro estava incorreto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória livre suficiente para atender à solicitação.<br/>                                            |



 

## <a name="remarks"></a>Comentários

A contagem de referência de **IStream** será incrementada para cada *ponteiro ppMem* adquirido.

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

 

 
