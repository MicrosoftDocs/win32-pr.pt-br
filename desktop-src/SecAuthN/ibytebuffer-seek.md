---
description: O método Seek altera o ponteiro de busca para um novo local relativo ao início do buffer, para o final do buffer ou para o ponteiro de busca atual.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'Método IByteBuffer:: Seek (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 70c4af327fad5014c5d6dec80dd29441f51a03639a108249991c83f53e5d2be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016246"
---
# <a name="ibytebufferseek-method"></a>Método IByteBuffer:: Seek

\[O método **Seek** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O método **Seek** altera o ponteiro de busca para um novo local relativo ao início do buffer, para o final do buffer ou para o ponteiro de busca atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dlibMove* \[ no\]
</dt> <dd>

O deslocamento a ser adicionado ao local indicado por *dwOrigin*. Se *dwOrigin* for \_ conjunto de busca de fluxo \_ , isso será interpretado como um valor não assinado em vez de assinada.

</dd> <dt>

*dwOrigin* \[ no\]
</dt> <dd>

Especifica a origem para o deslocamento especificado em *dlibMove*. A origem pode ser um dos valores na tabela a seguir.



| Valor                                                                                                                                                                | Significado                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <dt>**\_conjunto de busca de fluxo \_**</dt> </dl> | O novo ponteiro de busca é um deslocamento relativo ao início do fluxo. Nesse caso, o parâmetro *dlibMove* é a nova posição de busca relativa ao início do fluxo.<br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <dt>**\_pesquisa de busca de fluxo \_**</dt> </dl> | O novo ponteiro de busca é um deslocamento relativo ao local do ponteiro de busca atual. Nesse caso, o parâmetro *dlibMove* é o deslocamento assinado da posição de busca atual.<br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <dt>**fim do fluxo de \_ busca \_**</dt> </dl> | O novo ponteiro de busca é um deslocamento relativo ao final do fluxo. Nesse caso, o parâmetro *dlibMove* é a nova posição de busca relativa ao final do fluxo.<br/>             |



 

</dd> <dt>

*plibNewPosition* \[ fora\]
</dt> <dd>

Ponteiro para o local em que esse método grava o valor do novo ponteiro de busca do início do fluxo. Você pode definir esse ponteiro como **nulo** para indicar que você não está interessado nesse valor. Nesse caso, esse método não fornece o novo ponteiro de busca.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

O método **Seek** altera o ponteiro de busca para que as operações de leitura e gravação subsequentes possam ocorrer em um local diferente no objeto de fluxo. É um erro a ser buscado antes do início do fluxo. No entanto, não há um erro a ser buscado após o final do fluxo. A busca após o final do fluxo é útil para operações de gravação subsequentes, pois o fluxo nesse momento será estendido para a posição de busca imediatamente antes que a operação de gravação seja feita.

Você também pode usar esse método para obter o valor atual do ponteiro de busca chamando esse método com o parâmetro *dwOrigin* definido como Stream \_ Seek \_ cur e o parâmetro *dlibMove* definido como zero para que o ponteiro de busca não seja alterado. O ponteiro de busca atual é retornado no parâmetro *plibNewPosition* .

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o posicionamento do ponteiro de busca em um novo local.


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

