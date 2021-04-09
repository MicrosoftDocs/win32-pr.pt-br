---
description: O método CopyTo copia um número especificado de bytes do ponteiro de busca atual no objeto para o ponteiro de busca atual em outro objeto.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: 'Método IByteBuffer:: CopyTo (Scardssp. h)'
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
ms.openlocfilehash: 9f6b35a2cfa2de459bb5e7acfcb9853e83ae0a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171267"
---
# <a name="ibytebuffercopyto-method"></a>Método IByteBuffer:: CopyTo

\[O método **CopyTo** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O método **CopyTo** copia um número especificado de bytes do ponteiro de busca atual no objeto para o ponteiro de busca atual em outro objeto.

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

*pByteBuffer* \[ no\]
</dt> <dd>

Aponta para o fluxo de destino. O fluxo apontado por *pByteBuffer* pode ser um novo fluxo ou um clone do fluxo de origem.

</dd> <dt>

*CB* \[ no\]
</dt> <dd>

Número de bytes a serem copiados do fluxo de origem.

</dd> <dt>

*pcbRead* \[ fora\]
</dt> <dd>

Aponta para o local em que esse método grava o número real de bytes lidos da origem. Você pode definir esse ponteiro como **nulo** para indicar que você não está interessado nesse valor. Nesse caso, esse método não fornece o número real de bytes lidos.

</dd> <dt>

*pcbWritten* \[ fora\]
</dt> <dd>

Aponta para o local em que esse método grava o número real de bytes gravados no destino. Você pode definir esse ponteiro como **nulo** para indicar que você não está interessado nesse valor. Nesse caso, esse método não fornece o número real de bytes gravados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

Esse método copia os bytes especificados de um fluxo para outro. Ele também pode ser usado para copiar um fluxo para si mesmo. O ponteiro de busca em cada instância de fluxo é ajustado para o número de bytes lidos ou gravados.

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



 

