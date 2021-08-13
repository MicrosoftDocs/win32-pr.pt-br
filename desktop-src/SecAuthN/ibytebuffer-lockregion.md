---
description: Restringe o acesso a um intervalo especificado de bytes no objeto de buffer.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: Método IByteBuffer::LockRegion (Scardssp.h)
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
ms.openlocfilehash: 8575a568615a88552dd3907c7a5733c81dfe2d222661b4d8f9f82e32f0896ecf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482676"
---
# <a name="ibytebufferlockregion-method"></a>Método IByteBuffer::LockRegion

\[O **método LockRegion** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O **método LockRegion** restringe o acesso a um intervalo especificado de bytes no objeto de buffer.

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

*libOffset* \[ Em\]
</dt> <dd>

Inteiro que especifica o deslocamento de byte para o início do intervalo.

</dd> <dt>

*cb* \[ Em\]
</dt> <dd>

Inteiro que especifica o comprimento do intervalo, em bytes, a ser restrito.

</dd> <dt>

*dwLockType* \[ Em\]
</dt> <dd>

Especifica as restrições que estão sendo solicitadas ao acessar o intervalo. Esse pode ser um dos valores na tabela a seguir.



| Valor                                                                                                                                                            | Significado                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <dt>**GRAVAÇÃO \_ DE BLOQUEIO**</dt> </dl>             | O intervalo de bytes especificado pode ser aberto e ler qualquer número de vezes, mas a escrita no intervalo bloqueado é proibida, exceto para o proprietário que recebeu esse bloqueio.<br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <dt>**LOCK \_ EXCLUSIVE**</dt> </dl> | A escrita no intervalo especificado de bytes é proibida, exceto para o proprietário que recebeu esse bloqueio.<br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <dt>**LOCK \_ ONLYONCE**</dt> </dl>    | Se esse bloqueio for concedido, nenhum outro bloqueio LOCK \_ ONLYONCE poderá ser obtido no intervalo. Normalmente, esse tipo de bloqueio é um alias para algum outro tipo de bloqueio. Portanto, implementações específicas podem ter um comportamento adicional associado a esse tipo de bloqueio.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é **um HRESULT.** Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

O intervalo de byte pode se estender após a extremidade atual do fluxo. O bloqueio além do final de um fluxo é útil como um método de comunicação entre diferentes instâncias do fluxo sem alterar dados que, na verdade, fazem parte do fluxo.

Três tipos de bloqueio podem ser suportados: bloqueio para excluir outros autores, bloqueio para excluir outros leitores ou autores e bloqueio que permite que apenas um solicitante obtenha um bloqueio no intervalo determinado, que geralmente é um alias para um dos outros dois tipos de bloqueio. Uma determinada instância de fluxo pode dar suporte a qualquer um dos dois primeiros tipos ou ambos. O tipo de bloqueio é especificado por *dwLockType*, usando um valor da [**enumeração LOCKTYPE.**](/windows/win32/api/objidl/ne-objidl-locktype)

Qualquer região bloqueada com **LockRegion** posteriormente deve ser desbloqueada explicitamente chamando [**IByteBuffer::UnlockRegion**](ibytebuffer-unlockregion.md) com exatamente os mesmos valores para os parâmetros *libOffset*, *cb* e *dwLockType.* A região deve ser desbloqueada antes que o fluxo seja liberado. Duas regiões adjacentes não podem ser bloqueadas separadamente e desbloqueadas com uma única chamada de desbloqueio.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como restringir o acesso a um intervalo de bytes.


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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID IByteBuffer é definido como \_ E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

