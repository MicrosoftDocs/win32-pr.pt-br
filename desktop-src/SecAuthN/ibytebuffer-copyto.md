---
description: O método CopyTo copia um número especificado de bytes do ponteiro de busca atual no objeto para o ponteiro de busca atual em outro objeto.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: Método IByteBuffer::CopyTo (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4c4dc3861120d56dd5bff13fe1e77fd97e1fc32efed9622f18ee51b5160d1c35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417636"
---
# <a name="ibytebuffercopyto-method"></a>Método IByteBuffer::CopyTo

\[O **método CopyTo** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O **método CopyTo** copia um número especificado de bytes do ponteiro de busca atual no objeto para o ponteiro de busca atual em outro objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pByteBuffer* \[ Em\]
</dt> <dd>

Aponta para o fluxo de destino. O fluxo apontado por *pByteBuffer* pode ser um novo fluxo ou um clone do fluxo de origem.

</dd> <dt>

*cb* \[ Em\]
</dt> <dd>

Número de bytes a copiar do fluxo de origem.

</dd> <dt>

*pcbRead* \[ out\]
</dt> <dd>

Ponteiro para o local em que esse método grava o número real de bytes lidos da origem. Você pode definir esse ponteiro como **NULL** para indicar que não está interessado nesse valor. Nesse caso, esse método não fornece o número real de bytes lidos.

</dd> <dt>

*pcbWritten* \[ out\]
</dt> <dd>

Ponteiro para o local em que esse método grava o número real de bytes gravados no destino. Você pode definir esse ponteiro como **NULL** para indicar que não está interessado nesse valor. Nesse caso, esse método não fornece o número real de bytes gravados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é **um HRESULT.** Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

Esse método copia os bytes especificados de um fluxo para outro. Ele também pode ser usado para copiar um fluxo para si mesmo. O ponteiro seek em cada instância de fluxo é ajustado para o número de bytes lidos ou gravados.

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



 

