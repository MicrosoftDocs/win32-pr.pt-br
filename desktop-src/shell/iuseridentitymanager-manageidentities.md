---
description: 'IUserIdentityManager:: ManageIdentities não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.'
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'Método IUserIdentityManager:: ManageIdentities (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a816ee16e128b992b18be274d814fe3369e1a59c0204201a9c6bd4a6cbc23857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859234"
---
# <a name="iuseridentitymanagermanageidentities-method"></a>Método IUserIdentityManager:: ManageIdentities

\[**IUserIdentityManager:: ManageIdentities** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Exibe uma IU para o usuário, permitindo que o usuário gerencie identidades de usuário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Digite: **HWND**

Um valor de **HWND** que identifica uma janela que será colocada em primeiro plano depois que a interface do usuário for ignorada.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Sinalizadores opcionais para definir como o comportamento da interface do usuário se comportará. Defina como UIMI \_ criar \_ nova \_ identidade para solicitar que o usuário crie uma nova identidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

O resultado da operação de gerenciamento. Se for bem-sucedido, retornará S \_ OK. Caso contrário, ele retornará um dos seguintes códigos de erro.



| Código de retorno                                                                                            | Descrição                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_identidades E \_ desabilitadas**</dt> </dl> | O gerenciamento de identidades está desabilitado no sistema.<br/> |
| <dl> <dt>**E \_ usuário \_ cancelados**</dt> </dl>      | O usuário cancelou a caixa de diálogo.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fim do suporte do servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager:: logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**IUserIdentityManager:: fazer logoff**](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




