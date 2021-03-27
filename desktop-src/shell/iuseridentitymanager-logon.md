---
description: 'IUserIdentityManager:: não há suporte para logon e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.'
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'Método IUserIdentityManager:: logon (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eee6e0555d45d3f52173fce085d19c14f2ccfe8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089711"
---
# <a name="iuseridentitymanagerlogon-method"></a>Método IUserIdentityManager:: logon

\[**IUserIdentityManager::** não há suporte para logon e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Exibe uma IU para o usuário, permitindo que o usuário escolha uma identidade de usuário. Se for bem-sucedido, a identidade do usuário será registrada e recuperada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Tipo: **HWND**

Um valor de **HWND** que identifica uma janela que será colocada em primeiro plano depois que a interface do usuário de logon for ignorada.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Sinalizadores opcionais para definir como o comportamento da interface do usuário se comportará. Defina como UIL \_ forçar \_ a interface do usuário para forçar a exibição da interface do usuário, mesmo que uma identidade já tenha sido escolhida.

</dd> <dt>

*ppIdentity* \[ fora\]
</dt> <dd>

Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***

O endereço do ponteiro que recebe a identidade do usuário escolhida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Resultado da operação de logon. Se for bem-sucedido, retornará S \_ OK. Caso contrário, ele retornará um dos seguintes códigos de erro.



| Código de retorno                                                                                            | Description                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ usuário \_ cancelados**</dt> </dl>      | O usuário cancelou a operação de logon da IU.<br/>                               |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Não foi possível criar a identidade do usuário.<br/>                                          |
| <dl> <dt>**E \_ inesperado**</dt> </dl>           | A operação falhou inesperadamente.<br/>                                               |
| <dl> <dt>**\_identidades E \_ desabilitadas**</dt> </dl> | O gerenciamento de identidades está desabilitado no sistema.<br/>                                   |
| <dl> <dt>**S \_ identidades \_ desabilitadas**</dt> </dl> | O gerenciamento de identidades está desabilitado no sistema.<br/>                                   |
| <dl> <dt>**\_alteração de identidade E \_**</dt> </dl>   | O sistema está atualmente alternando identidades e não pode concluir a operação.<br/> |



 

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager:: fazer logoff**](iuseridentitymanager-logoff.md)
</dt> <dt>

[**IUserIdentityManager::ManageIdentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




