---
description: GetCount não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: 'Método IEnumUserIdentity:: GetCount (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.GetCount
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 43355a9585fc4099c8649f7df506ff3495a53944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296726"
---
# <a name="ienumuseridentitygetcount-method"></a>Método IEnumUserIdentity:: GetCount

\[**GetCount** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Obtém a contagem de identidades de usuário atualmente no sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pnCount* \[ fora\]
</dt> <dd>

Tipo: **ULONG \** _

Ponteiro para um _ *ULONG** que recebe a contagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se o suporte para várias identidades de usuário estiver desabilitado, o *pnCount* receberá um valor de 1.

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

[**IEnumUserIdentity:: Next**](ienumuseridentity-next.md)
</dt> </dl>

 

 




