---
description: 'IEnumUserIdentity:: Next não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.'
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'Método IEnumUserIdentity:: Next (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 763b2b4a612596c5f02a9826ad2e9c09ab8e4b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988965"
---
# <a name="ienumuseridentitynext-method"></a>Método IEnumUserIdentity:: Next

\[**IEnumUserIdentity:: Next** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Preterido. Recupera uma matriz de interfaces de identidade do usuário da enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*celt* \[ no\]
</dt> <dd>

Tipo: **ULONG**

Um valor **ULONG** que representa o número de interfaces a serem recuperadas.

</dd> <dt>

*rgelt* \[ fora\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

O endereço de um ponteiro que recebe as interfaces.

</dd> <dt>

*pceltFetched* \[ fora\]
</dt> <dd>

Tipo: **ULONG \** _

O endereço de um ponteiro que recebe o número de interfaces recuperadas com êxito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

[**IEnumUserIdentity**](ienumuseridentity.md) mantém uma contagem interna que especifica qual interface está próxima de ser recuperada. Várias chamadas para este método não redefinirão essa contagem. Para redefinir a contagem, chame [**IEnumUserIdentity:: Reset**](ienumuseridentity-reset.md). Para incrementar a contagem sem recuperar interfaces, chame [**IEnumUserIdentity:: Skip**](ienumuseridentity-skip.md).

O valor de *celt* não deve exceder o valor retornado por [**IEnumUserIdentity:: GetCount**](ienumuseridentity-getcount.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                  |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity:: Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**IEnumUserIdentity:: Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity:: GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
