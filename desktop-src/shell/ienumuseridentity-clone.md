---
description: Não há suporte para IEnumUserIdentity::Clone e podem ser alterados ou não disponíveis no futuro. Em vez disso, use Contas de Usuário com Troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: Método IEnumUserIdentity::Clone (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Clone
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3e6b0903029fa44e26651ad1df99ceb0c6bd83253bcd1d139bb6513d65e3ca3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009406"
---
# <a name="ienumuseridentityclone-method"></a>Método IEnumUserIdentity::Clone

\[**Não há suporte para IEnumUserIdentity::Clone** e podem ser alterados ou não disponíveis no futuro. Em vez disso, [use Contas de Usuário com a Opção de Usuário Rápida e Área de Trabalho Remota](fastuserswitching.md).\]

Obtém uma cópia da enumeração atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppenum* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***

O endereço de um ponteiro que recebe uma cópia dessa enumeração.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

[**IEnumUserIdentity**](ienumuseridentity.md) mantém uma contagem interna que especifica qual interface é a próxima a ser recuperada. O valor dessa contagem será aplicado à interface recebida pelo *ppenum*. Para redefinir a contagem, chame [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).

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
</dt> </dl>

 

 




