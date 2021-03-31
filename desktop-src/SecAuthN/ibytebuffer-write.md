---
description: O método Write grava um número especificado de bytes no objeto de fluxo a partir do ponteiro de busca atual.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: 'Método IByteBuffer:: Write (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b5f9b60a296041a18fbd850f1405088f5b0da2ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829764"
---
# <a name="ibytebufferwrite-method"></a>Método IByteBuffer:: Write

\[O método **Write** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O método **Write** grava um número especificado de bytes no objeto de fluxo a partir do ponteiro de busca atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pByte* \[ no\]
</dt> <dd>

Endereço do buffer que contém os dados que serão gravados no fluxo. Um ponteiro válido deve ser fornecido para esse parâmetro mesmo quando *CB* for zero.

</dd> <dt>

*CB* \[ no\]
</dt> <dd>

Número de bytes de dados para tentar gravar no fluxo. Esse parâmetro pode ser zero.

</dd> <dt>

*pcbWritten* \[ fora\]
</dt> <dd>

Endereço de uma variável **longa** em que esse método grava o número real de bytes gravados no objeto de fluxo. O chamador pode definir esse ponteiro como **NULL**; nesse caso, esse método não fornece o número real de bytes gravados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

O método **IByteBuffer:: Write** grava os dados especificados em um objeto Stream. O ponteiro de busca é ajustado para o número de bytes realmente gravados. O número de bytes realmente gravados é retornado no parâmetro *pcbWritten* . Se a contagem de bytes for zero bytes, a operação de gravação não terá nenhum efeito.

Se o ponteiro de busca estiver no momento após o final do fluxo e a contagem de bytes for diferente de zero, esse método aumentará o tamanho do fluxo para o ponteiro de busca e gravará os bytes especificados a partir do ponteiro de busca. Os bytes de preenchimento gravados no fluxo não são inicializados para nenhum valor específico. Isso é o mesmo que o comportamento final do arquivo no sistema de arquivos FAT do MS-DOS.

Com uma contagem de bytes zero e um ponteiro de busca após o final do fluxo, esse método não cria os bytes de preenchimento para aumentar o fluxo para o ponteiro de busca. Nesse caso, você deve chamar o método [**IByteBuffer:: SetSize**](ibytebuffer-setsize.md) para aumentar o tamanho do fluxo e gravar os bytes de preenchimento.

O parâmetro *pcbWritten* pode ter um valor mesmo se ocorrer um erro.

Na implementação fornecida COM, os objetos de fluxo não são esparsos. Todos os bytes de preenchimento são eventualmente alocados no disco e atribuídos ao fluxo.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a gravação de bytes no objeto de fluxo.


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
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



 

