---
description: O método Initialize prepara o objeto IByteBuffer para uso. Esse método deve ser chamado antes de chamar qualquer outro método na interface IByteBuffer.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: Método IByteBuffer::Initialize (Scardssp.h)
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
ms.openlocfilehash: 28a525b26d49dd5df8a2be3ba6a5af5a16459c26e191368badae34ca381488e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417626"
---
# <a name="ibytebufferinitialize-method"></a>Método IByteBuffer::Initialize

\[O **método Initialize** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O **método Initialize** prepara o [**objeto IByteBuffer**](ibytebuffer.md) para uso. Esse método deve ser chamado antes de chamar qualquer outro método na interface **IByteBuffer.**

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lSize* \[ Em\]
</dt> <dd>

Tamanho inicial, em bytes, dos dados que o fluxo deve conter.

</dd> <dt>

*pData* \[ Em\]
</dt> <dd>

Se não **for NULL,** os dados iniciais a gravar no fluxo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é **um HRESULT.** Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

Ao usar um novo [**fluxo IByteBuffer,**](ibytebuffer.md) chame esse método antes de usar qualquer um dos outros **métodos IByteBuffer.**

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a inicialização do [**objeto IByteBuffer.**](ibytebuffer.md)


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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID IByteBuffer é definido como \_ E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

