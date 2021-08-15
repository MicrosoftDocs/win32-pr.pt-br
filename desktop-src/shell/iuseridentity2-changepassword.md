---
description: Não há suporte para ChangePassword e pode ser alterado ou não disponível no futuro. Em vez disso, use Contas de Usuário com Troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: Método IUserIdentity2::ChangePassword (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d892fd3f676183864d72d905b72cea2f01643211314fc293b1cd76e5d70fc237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092693"
---
# <a name="iuseridentity2changepassword-method"></a>Método IUserIdentity2::ChangePassword

\[**Não há suporte para ChangePassword** e pode ser alterado ou não disponível no futuro. Em vez disso, [use Contas de Usuário com a Opção de Usuário Rápida e Área de Trabalho Remota](fastuserswitching.md).\]

Define uma nova senha para a identidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szOldPass* \[ Em\]
</dt> <dd>

Tipo: **WCHAR \***

A cadeia de caracteres largos que contém a senha atualmente associada à identidade.

</dd> <dt>

*szNewPass* \[ Em\]
</dt> <dd>

Tipo: **WCHAR \***

A cadeia de caracteres largos que contém a nova senha a ser associada à identidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O valor de *szOldPass* deve corresponder à senha atual da identidade para *que szNewPass* seja aplicado. Um valor incorreto de *szOldPass* resultará em um valor de retorno de E \_ FAIL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Fim do suporte ao cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fim do suporte ao servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



 

 




