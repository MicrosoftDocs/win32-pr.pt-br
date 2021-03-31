---
description: Libera o ponteiro de byte apontando para o bloco de memória HGLOBAL gerenciado por uma interface COM de IStream.
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: 'Método ISCardTypeConv:: FreeIStreamMemoryPtr (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 12912b8130ed6e1ccaa995f88069b59e96f57c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662280"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a>Método ISCardTypeConv:: FreeIStreamMemoryPtr

\[O método **FreeIStreamMemoryPtr** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **FreeIStreamMemoryPtr** libera o ponteiro de byte apontando para o bloco de memória HGLOBAL gerenciado por uma interface com de **IStream** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStrm* \[ no\]
</dt> <dd>

Ponteiro para a interface **IStream** que gerencia o bloco de memória apontado pelo *pMem*.

</dd> <dt>

*pMem* \[ no\]
</dt> <dd>

Ponteiro para o bloco de memória gerenciado pela interface **IStream** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memória alocada com êxito.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Há algo errado com um ou mais dos parâmetros passados para a função.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um parâmetro de tipo de ponteiro estava incorreto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória livre suficiente para atender à solicitação.<br/>                                            |



 

## <a name="remarks"></a>Comentários

Essa função libera completamente e limpa o ponteiro de byte apontando para o bloco de memória HGLOBAL gerenciado pela interface **IStream** . O ponteiro de byte é adquirido por uma chamada para [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).

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
</dt> <dt>

[**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
