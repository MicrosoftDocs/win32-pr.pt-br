---
description: Restringe o acesso a um intervalo especificado de bytes no objeto de buffer.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'Método IByteBuffer:: LockRegion (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171264"
---
# <a name="ibytebufferlockregion-method"></a>Método IByteBuffer:: LockRegion

\[O método **LockRegion** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O método **LockRegion** restringe o acesso a um intervalo especificado de bytes no objeto buffer.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*libOffset* \[ no\]
</dt> <dd>

Inteiro que especifica o deslocamento de byte para o início do intervalo.

</dd> <dt>

*CB* \[ no\]
</dt> <dd>

Inteiro que especifica o comprimento do intervalo, em bytes, a ser restringido.

</dd> <dt>

*dwLockType* \[ no\]
</dt> <dd>

Especifica as restrições que estão sendo solicitadas ao acessar o intervalo. Isso pode ser um dos valores na tabela a seguir.



| Valor                                                                                                                                                            | Significado                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <dt>**BLOQUEAR \_ gravação**</dt> </dl>             | O intervalo especificado de bytes pode ser aberto e lido várias vezes, mas a gravação no intervalo bloqueado é proibida, exceto pelo proprietário que recebeu esse bloqueio.<br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <dt>**BLOQUEIO \_ exclusivo**</dt> </dl> | A gravação no intervalo de bytes especificado é proibida, exceto pelo proprietário que recebeu esse bloqueio.<br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <dt>**BLOQUEAR \_ ONLYONCE**</dt> </dl>    | Se esse bloqueio for concedido, nenhum outro \_ bloqueio de ONLYONCE de bloqueio poderá ser obtido no intervalo. Geralmente, esse tipo de bloqueio é um alias para algum outro tipo de bloqueio. Portanto, implementações específicas podem ter um comportamento adicional associado a esse tipo de bloqueio.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

O intervalo de bytes pode ultrapassar a extremidade atual do fluxo. O bloqueio além do fim de um fluxo é útil como um método de comunicação entre diferentes instâncias do fluxo sem alterar os dados que realmente fazem parte do fluxo.

Há suporte para três tipos de bloqueio: bloqueio para excluir outros gravadores, bloqueio para excluir outros leitores ou gravadores e bloqueio que permite que apenas um solicitante obtenha um bloqueio no intervalo determinado, que geralmente é um alias para um dos outros dois tipos de bloqueio. Uma determinada instância de fluxo pode dar suporte a qualquer um dos dois primeiros tipos, ou ambos. O tipo de bloqueio é especificado por *dwLockType*, usando um valor da enumeração [**LockType**](/windows/win32/api/objidl/ne-objidl-locktype) .

Qualquer região bloqueada com **LockRegion** deve ser desbloqueada mais tarde chamando [**IByteBuffer:: UnlockRegion**](ibytebuffer-unlockregion.md) com exatamente os mesmos valores para os parâmetros *libOffset*, *CB* e *dwLockType* . A região deve ser desbloqueada antes de o fluxo ser liberado. Duas regiões adjacentes não podem ser bloqueadas separadamente e desbloqueadas com uma única chamada de desbloqueio.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a restrição de acesso a um intervalo de bytes.


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
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



 

