---
description: O método clone cria um novo objeto com seu próprio ponteiro de busca que faz referência aos mesmos bytes do objeto IByteBuffer original.
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'Método IByteBuffer:: clone (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d994ef55665b03da2a7d657689682f893fdf071f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170822"
---
# <a name="ibytebufferclone-method"></a>Método IByteBuffer:: clone

\[O método **clone** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O método **clone** cria um novo objeto com seu próprio ponteiro de busca que faz referência aos mesmos bytes do objeto [**IByteBuffer**](ibytebuffer.md) original.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppByteBuffer* \[ fora\]
</dt> <dd>

Quando bem-sucedido, aponta para o local de um ponteiro [**IByteBuffer**](ibytebuffer.md) para o novo objeto Stream. Quando você terminar de usar o ponteiro **IByteBuffer** , libere-o chamando a função [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . Se ocorrer um erro, esse parâmetro será **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

Esse método cria um novo objeto de fluxo para acessar os mesmos bytes, mas usando um ponteiro de busca separado. O novo objeto de fluxo vê os mesmos dados que o objeto de fluxo de origem. As alterações gravadas em um objeto ficam imediatamente visíveis no outro. O bloqueio de intervalo é compartilhado entre os objetos de fluxo.

A configuração inicial do ponteiro de busca na instância de fluxo clonado é igual à configuração atual do ponteiro de busca no fluxo original no momento da operação de clonagem.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a clonagem da interface [**IByteBuffer**](ibytebuffer.md) .


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
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



 

