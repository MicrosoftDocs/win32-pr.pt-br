---
description: O método Commit garante que todas as alterações feitas em um objeto aberto no modo transacionado sejam refletidas no armazenamento pai.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: Método IByteBuffer::Commit (Scardssp.h)
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
ms.openlocfilehash: af165e6f0a805532eade820dcb67968a77186cee3f90cfc48a240d387b1f31b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127406"
---
# <a name="ibytebuffercommit-method"></a>Método IByteBuffer::Commit

\[O **método Commit** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O **método Commit** garante que todas as alterações feitas em um objeto aberto no modo transacionado sejam refletidas no armazenamento pai.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*grfCommitFlags* \[ Em\]
</dt> <dd>

Controla como as alterações no objeto de fluxo são confirmadas. Para uma definição desses valores, consulte a enumeração STGC.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é **um HRESULT.** Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

Esse método garante que as alterações em um objeto de fluxo aberto no modo transacionado sejam refletidas no armazenamento pai. As alterações feitas no fluxo desde que ele foi aberto ou confirmado pela última vez são refletidas no objeto de armazenamento pai. Se o pai for aberto no modo transacionado, o pai ainda poderá reverter posteriormente revertendo as alterações para esse objeto de fluxo. A implementação de arquivo composto não dá suporte à abertura de fluxos no modo transacionado, portanto, esse método tem muito pouco efeito além de liberar buffers de memória.

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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID IByteBuffer é definido como \_ E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

