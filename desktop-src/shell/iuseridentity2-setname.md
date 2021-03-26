---
description: 'IUserIdentity2:: SetName não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.'
ms.assetid: 1c9c3beb-fa1c-4b4d-9cfd-656b97949036
title: 'Método IUserIdentity2:: SetName (Msident. h)'
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
ms.openlocfilehash: 0b0fd06ef4b582987e41c2343f2d4596db6b8528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968022"
---
# <a name="iuseridentity2setname-method"></a>Método IUserIdentity2:: SetName

\[**IUserIdentity2:: SetName** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Define o nome de exibição da identidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetName(
  [in] WCHAR *pszName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszName* \[ no\]
</dt> <dd>

Tipo: **WCHAR \** _

A cadeia de caracteres largos que contém o novo nome da identidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**GetName**](iuseridentity-getname.md)
</dt> </dl>

 

 




