---
description: Adquire um ponteiro de byte para o bloco de memória HGLOBAL que é gerenciado pela interface COM de IStream.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: 'Método ISCardTypeConv:: GetAtIStreamMemory (Scarddat. h)'
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
ms.openlocfilehash: bdd828921f18c3d06edd2d41da189260a4ed4394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646783"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a>Método ISCardTypeConv:: GetAtIStreamMemory

\[O método **GetAtIStreamMemory** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **GetAtIStreamMemory** adquire um ponteiro de byte para o bloco de memória HGLOBAL que é gerenciado pela interface com de **IStream** .

Essa é uma maneira de obter a memória sob o **IStream** sem ter que obter o valor de sizeof para o bloco de memória em bytes e ler os bytes em uma matriz de bytes temporária usando a interface **IStream** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStrm* \[ no\]
</dt> <dd>

Um ponteiro para a interface com **IStream** que gerencia o bloco de memória HGLOBAL.

</dd> <dt>

*ppMem* \[ fora\]
</dt> <dd>

Um ponteiro para o primeiro byte do bloco de memória HGLOBAL se for bem-sucedido; caso contrário, **NULL** se a operação falhar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memória alocada com êxito.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Há algo errado com um ou mais dos parâmetros passados para a função.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um parâmetro de tipo de ponteiro estava incorreto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória livre suficiente para atender à solicitação.<br/>                                            |



 

## <a name="remarks"></a>Comentários

A contagem de referência de **IStream** será incrementada para cada ponteiro *ppMem* adquirido.

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

 

 
