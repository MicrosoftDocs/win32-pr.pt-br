---
description: Não há suporte para ChangePassword e ele pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'Método IUserIdentity2:: ChangePassword (Msident. h)'
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
ms.openlocfilehash: dd4b858924e4b042b3d7a0636d90eb582e9506df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967485"
---
# <a name="iuseridentity2changepassword-method"></a>Método IUserIdentity2:: ChangePassword

\[Não há suporte para **ChangePassword** e ele pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

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

*szOldPass* \[ no\]
</dt> <dd>

Tipo: **WCHAR \** _

A cadeia de caracteres largos que contém a senha atualmente associada à identidade.

</dd> <dt>

_szNewPass * \[ in\]
</dt> <dd>

Tipo: **WCHAR \** _

A cadeia de caracteres largos que contém a nova senha a ser associada à identidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O valor de *szOldPass* deve corresponder à senha atual da identidade para *szNewPass* a ser aplicado. Um valor incorreto de *szOldPass* resultará em um valor de retorno de E \_ falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fim do suporte do servidor<br/>    | Windows 2000 Server<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



 

 




