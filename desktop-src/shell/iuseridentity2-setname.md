---
description: Não há suporte para IUserIdentity2::SetName e pode ser alterado ou não disponível no futuro. Em vez disso, use Contas de Usuário com Troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: 1c9c3beb-fa1c-4b4d-9cfd-656b97949036
title: Método IUserIdentity2::SetName (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.SetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 32c375f37fbc0bc6352a79c9eb37be56578b236f6131c4ead1ea721cc53ce5e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220068"
---
# <a name="iuseridentity2setname-method"></a>Método IUserIdentity2::SetName

\[**Não há suporte para IUserIdentity2::SetName** e pode ser alterado ou não disponível no futuro. Em vez disso, [use Contas de Usuário com a Opção de](fastuserswitching.md)Usuário Rápida e Área de Trabalho Remota .\]

Define o nome de exibição da identidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetName(
  [in] WCHAR *pszName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszName* \[ Em\]
</dt> <dd>

Tipo: **WCHAR \***

A cadeia de caracteres largos que contém o novo nome da identidade.

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
| parâmetro<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**GetName**](iuseridentity-getname.md)
</dt> </dl>

 

 




