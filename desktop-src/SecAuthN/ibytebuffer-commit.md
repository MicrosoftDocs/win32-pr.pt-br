---
description: O método Commit garante que todas as alterações feitas em um objeto aberto no modo transacionado sejam refletidas no armazenamento pai.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: 'Método IByteBuffer:: Commit (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 066925361d0ee4391bcd1eaafe33e0ae2d4b9120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750505"
---
# <a name="ibytebuffercommit-method"></a>Método IByteBuffer:: Commit

\[O método **Commit** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O método **Commit** garante que todas as alterações feitas em um objeto aberto no modo transacionado sejam refletidas no armazenamento pai.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*grfCommitFlags* \[ no\]
</dt> <dd>

Controla como as alterações no objeto de fluxo são confirmadas. Para obter uma definição desses valores, consulte a enumeração STGC.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

Esse método garante que as alterações em um objeto de fluxo aberto no modo transacionado sejam refletidas no armazenamento pai. As alterações que foram feitas no fluxo desde que ela foi aberta ou confirmadas pela última vez são refletidas no objeto de armazenamento pai. Se o pai for aberto no modo transacionado, o pai ainda poderá ser revertido em um momento posterior, revertendo as alterações para esse objeto de fluxo. A implementação do arquivo composto não oferece suporte à abertura de fluxos no modo transacionado, portanto, esse método tem muito pouco efeito além de liberar buffers de memória.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a confirmação de alterações no armazenamento.


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

