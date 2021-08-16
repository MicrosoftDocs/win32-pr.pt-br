---
description: Não há suporte para GetCount e podem ser alterados ou não disponíveis no futuro. Em vez disso, use Contas de Usuário com Troca rápida de usuários e Área de Trabalho Remota.
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: Método IEnumUserIdentity::GetCount (Msident.h)
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
ms.openlocfilehash: e4848ec183096b37adbc04521fab04fd800d3783377d1e14b3abd068819648ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678933"
---
# <a name="ienumuseridentitygetcount-method"></a>Método IEnumUserIdentity::GetCount

\[Não há suporte para **GetCount** e podem ser alterados ou não disponíveis no futuro. Em vez disso, [use Contas de Usuário com a Opção de](fastuserswitching.md)Usuário Rápida e Área de Trabalho Remota .\]

Obtém a contagem de identidades de usuário atualmente no sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pnCount* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

Ponteiro para um **ULONG** que recebe a contagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Se o suporte para várias identidades de usuário estiver desabilitado, *pnCount* receberá um valor de 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                  |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity::Next**](ienumuseridentity-next.md)
</dt> </dl>

 

 




