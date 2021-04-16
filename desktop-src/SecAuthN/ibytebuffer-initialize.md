---
description: O método Initialize prepara o objeto IByteBuffer para uso. Esse método deve ser chamado antes de chamar qualquer outro método na interface IByteBuffer.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'Método IByteBuffer:: Initialize (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 245f9282174ddeef66b130597f0f20ddf21ededc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747855"
---
# <a name="ibytebufferinitialize-method"></a>Método IByteBuffer:: Initialize

\[O método **Initialize** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O método **Initialize** prepara o objeto [**IByteBuffer**](ibytebuffer.md) para uso. Esse método deve ser chamado antes de chamar qualquer outro método na interface **IByteBuffer** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lSize* \[ no\]
</dt> <dd>

Tamanho inicial, em bytes, dos dados que o fluxo deve conter.

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Se não for **NULL**, os dados iniciais a serem gravados no fluxo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

Ao usar um novo fluxo de [**IByteBuffer**](ibytebuffer.md) , chame esse método antes de usar qualquer um dos outros métodos de **IByteBuffer** .

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a inicialização do objeto [**IByteBuffer**](ibytebuffer.md) .


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
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



 

