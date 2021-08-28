---
description: Não há suporte para logoff e podem ser alterados ou não disponíveis no futuro. Em vez disso, use Contas de Usuário com Troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: e03fb15c-47d3-40ba-ae70-b7b0ba010004
title: Método IUserIdentityManager::Logoff (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logoff
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 6011bf839e2f91b3eb835cfe295e0c1845a6c6697a262c0f9bf7525d6c157565
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884056"
---
# <a name="iuseridentitymanagerlogoff-method"></a>Método IUserIdentityManager::Logoff

\[**Não há** suporte para logoff e podem ser alterados ou não disponíveis no futuro. Em vez disso, use [Contas de Usuário com a Opção de Usuário Rápida e Área de Trabalho Remota](fastuserswitching.md).\]

Preterido. Faça logoff da identidade atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Logoff(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ Em\]
</dt> <dd>

Digite: **HWND**

Um **valor HWND** que identifica uma janela que será levada para o primeiro plano quando o logoff for concluído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IUserIdentityManager::Logon**](iuseridentitymanager-logon.md)
</dt> <dt>

[**IUserIdentityManager::ManageIdentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




