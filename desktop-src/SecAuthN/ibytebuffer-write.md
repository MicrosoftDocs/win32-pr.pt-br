---
description: O método Write grava um número especificado de bytes no objeto de fluxo começando no ponteiro de busca atual.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: Método IByteBuffer::Write (Scardssp.h)
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
ms.openlocfilehash: 0033d4f4ee03629d2bedf9f232a43607100bcdca8bfaab457c2236bbfad603d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127346"
---
# <a name="ibytebufferwrite-method"></a>Método IByteBuffer::Write

\[O **método** Write está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O **método Write** grava um número especificado de bytes no objeto de fluxo começando no ponteiro de busca atual.

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

*pByte* \[ Em\]
</dt> <dd>

Endereço do buffer que contém os dados que devem ser gravados no fluxo. Um ponteiro válido deve ser fornecido para esse parâmetro mesmo quando *cb* é zero.

</dd> <dt>

*cb* \[ Em\]
</dt> <dd>

Número de bytes de dados a tentar gravar no fluxo. Esse parâmetro pode ser zero.

</dd> <dt>

*pcbWritten* \[ out\]
</dt> <dd>

Endereço de uma **variável LONG** em que esse método grava o número real de bytes gravados no objeto de fluxo. O chamador pode definir esse ponteiro como **NULL,** nesse caso, esse método não fornece o número real de bytes gravados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é **um HRESULT.** Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

O **método IByteBuffer::Write** grava os dados especificados em um objeto de fluxo. O ponteiro seek é ajustado para o número de bytes realmente gravados. O número de bytes realmente gravados é retornado no *parâmetro pcbWritten.* Se a contagem de bytes for zero bytes, a operação de gravação não terá nenhum efeito.

Se o ponteiro seek estiver atualmente após o final do fluxo e a contagem de bytes for diferente de zero, esse método aumentará o tamanho do fluxo para o ponteiro de busca e grava os bytes especificados começando no ponteiro de busca. Os bytes de preenchimento gravados no fluxo não são inicializados para nenhum valor específico. Isso é o mesmo que o comportamento de fim de arquivo no sistema de arquivos FAT do MS-DOS.

Com uma contagem de bytes zero e um ponteiro de busca após o final do fluxo, esse método não cria os bytes de preenchimento para aumentar o fluxo para o ponteiro de busca. Nesse caso, você deve chamar o método [**IByteBuffer::SetSize**](ibytebuffer-setsize.md) para aumentar o tamanho do fluxo e gravar os bytes de preenchimento.

O *parâmetro pcbWritten* pode ter um valor mesmo se ocorrer um erro.

Na implementação fornecida pelo COM, os objetos de fluxo não são esparsos. Todos os bytes de preenchimento são eventualmente alocados no disco e atribuídos ao fluxo.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a escrita de bytes no objeto de fluxo.


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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID IByteBuffer é definido como \_ E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

