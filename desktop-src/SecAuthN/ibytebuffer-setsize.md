---
description: O método setSize altera o tamanho do objeto de fluxo.
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'Método IByteBuffer:: SetSize (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 85a6abc11f3e007f3c8d1057cb5c8785c8519ebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922525"
---
# <a name="ibytebuffersetsize-method"></a>Método IByteBuffer:: SetSize

\[O método **SetSize** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O método **SetSize** altera o tamanho do objeto de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*libNewSize* \[ no\]
</dt> <dd>

Novo tamanho do fluxo como um número de bytes

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

O método **IByteBuffer:: SetSize** altera o tamanho do objeto de fluxo. Chame esse método para alocar espaço para o fluxo. Se o parâmetro *libNewSize* for maior que o tamanho atual do fluxo, o fluxo será estendido para o tamanho indicado preenchendo o espaço intermediário com bytes de valor indefinido. Essa operação é semelhante ao método [**IByteBuffer:: Write**](ibytebuffer-write.md) se o ponteiro de busca estiver além do fim do fluxo atual.

Se o parâmetro *libNewSize* for menor do que o fluxo atual, o fluxo será truncado para o tamanho indicado.

O ponteiro de busca não é afetado pela alteração no tamanho do fluxo.

Chamar **IByteBuffer:: SetSize** pode ser uma maneira eficaz de tentar obter uma grande parte do espaço contíguo.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a configuração do tamanho do buffer.


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
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



 

