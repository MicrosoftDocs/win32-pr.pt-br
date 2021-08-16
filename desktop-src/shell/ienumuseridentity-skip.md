---
description: Não há suporte para IEnumUserIdentity::Skip e pode ser alterado ou não disponível no futuro. Em vez disso, use Contas de Usuário com Troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: Método IEnumUserIdentity::Skip (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Skip
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: ced6a1a9ce463f82b6b33275339216edabc02737928e985a294154e579523575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678923"
---
# <a name="ienumuseridentityskip-method"></a>Método IEnumUserIdentity::Skip

\[Não há suporte para **IEnumUserIdentity::Skip** e pode ser alterado ou não disponível no futuro. Em vez disso, [use Contas de Usuário com a Opção de Usuário Rápida e Área de Trabalho Remota](fastuserswitching.md).\]

Ignora um determinado número de interfaces de identidade do usuário na enumeração. Usado ao recuperar interfaces.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ao mesmo tempo* \[ Em\]
</dt> <dd>

Tipo: **ULONG**

O número de interfaces a ignorar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

[**IEnumUserIdentity**](ienumuseridentity.md) mantém uma contagem interna que especifica qual interface é a próxima a ser recuperada. Para incrementar essa contagem sem recuperar interfaces, chame esse método. Para redefinir a contagem, chame [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).

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

[**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity::Next**](ienumuseridentity-next.md)
</dt> <dt>

[**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 




