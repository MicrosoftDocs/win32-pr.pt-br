---
description: Redefine a contagem interna de interfaces recuperadas na enumeração.
ms.assetid: fd79b4be-cc0c-49b3-9874-384858e21ecf
title: 'Método IEnumUserIdentity:: Reset (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Reset
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: df70048760af47b380308eddab4ef5c044c8f6881374c83002944d6d76836ed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969415"
---
# <a name="ienumuseridentityreset-method"></a>Método IEnumUserIdentity:: Reset

\[**IEnumUserIdentity:: Reset** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Redefine a contagem interna de interfaces recuperadas na enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

[**IEnumUserIdentity**](ienumuseridentity.md) mantém uma contagem interna que especifica qual interface está próxima de ser recuperada. Chamar esse método irá redefinir o valor dessa contagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                  |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity:: Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**IEnumUserIdentity:: GetCount**](ienumuseridentity-getcount.md)
</dt> <dt>

[**IEnumUserIdentity:: Next**](ienumuseridentity-next.md)
</dt> </dl>

 

 




