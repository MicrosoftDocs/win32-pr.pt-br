---
description: O método stat recupera informações estatísticas do objeto Stream.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'Método IByteBuffer:: stat (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bbbf033fc9ad5a25b3bcf5c22028ac1237f46c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752229"
---
# <a name="ibytebufferstat-method"></a>Método IByteBuffer:: stat

\[O método **stat** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

O método **stat** recupera informações estatísticas do objeto Stream.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStatStg* \[ fora\]
</dt> <dd>

Aponta para uma estrutura **STATSTRUCT** em que esse método coloca informações sobre este objeto de fluxo. Esse ponteiro será **nulo** se ocorrer um erro.

</dd> <dt>

*grfStatFlag* \[ no\]
</dt> <dd>

Especifica que esse método não retorna alguns dos campos na estrutura **STATSTRUCT** , salvando assim uma operação de alocação de memória. Os valores são obtidos da enumeração [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag)

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um **HRESULT**. Um valor de S \_ OK indica que a chamada foi bem-sucedida.

## <a name="remarks"></a>Comentários

O método **IByteBuffer:: stat** recupera um ponteiro para a estrutura **STATSTRUCT** que contém informações sobre esse fluxo aberto.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a recuperação de informações estatísticas do fluxo.


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
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



 

