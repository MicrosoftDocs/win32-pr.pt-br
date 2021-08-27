---
description: 'Remove a restrição de acesso em um intervalo de bytes anteriormente restritos usando IByteBuffer:: LockRegion.'
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'Método IByteBuffer:: UnlockRegion (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 798569621c1a46e73ea6fd8e2f4f3333c3a0cbcef32618797fcba39d35b55bf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127386"
---
# <a name="ibytebufferunlockregion-method"></a>Método IByteBuffer:: UnlockRegion

\[O método **UnlockRegion** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O método **UnlockRegion** remove a restrição de acesso em um intervalo de bytes anteriormente restringido usando [**IByteBuffer:: LockRegion**](ibytebuffer-lockregion.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*libOffset* \[ no\]
</dt> <dd>

Deslocamento de byte para o início do intervalo.

</dd> <dt>

*CB* \[ no\]
</dt> <dd>

Comprimento, em bytes, do intervalo a ser restringido.

</dd> <dt>

*dwLockType* \[ no\]
</dt> <dd>

Restrições de acesso previamente colocadas no intervalo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

O método **IByteBuffer:: UnlockRegion** desbloqueia uma região bloqueada anteriormente usando o método [**IByteBuffer:: LockRegion**](ibytebuffer-lockregion.md) . As regiões bloqueadas devem ser desbloqueadas mais tarde chamando **IByteBuffer:: UnlockRegion** com exatamente os mesmos valores para os parâmetros *libOffset*, *CB* e *dwLockType* . A região deve ser desbloqueada antes de o fluxo ser liberado. Duas regiões adjacentes não podem ser bloqueadas separadamente e desbloqueadas com uma única chamada de desbloqueio.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o desbloqueio de um intervalo de bytes.


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
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



 

