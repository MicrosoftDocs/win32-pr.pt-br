---
description: Não há suporte para IUserIdentity::GetName e pode ser alterado ou não disponível no futuro. Em vez disso, use Contas de Usuário com Troca rápida de usuários e Área de Trabalho Remota.
ms.assetid: 4db24dd2-d2b8-4a58-9c16-0e721bc195da
title: Método IUserIdentity::GetName (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 035f7c61290fb60e70821f0a43676c41dca0fc92cebc8ecfb963bb757ab47a5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661186"
---
# <a name="iuseridentitygetname-method"></a>Método IUserIdentity::GetName

\[**Não há suporte para IUserIdentity::GetName** e pode ser alterado ou não disponível no futuro. Em vez disso, [use Contas de Usuário com a Opção de](fastuserswitching.md)Usuário Rápida e Área de Trabalho Remota .\]

Obtém o nome associado a essa identidade de usuário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetName(
  [in] WCHAR *pszName,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszName* \[ Em\]
</dt> <dd>

Tipo: **WCHAR \***

Um ponteiro para uma cadeia de caracteres largos que recebe o nome dessa identidade de usuário.

</dd> <dt>

*ulBuffSize* \[ Em\]
</dt> <dd>

Tipo: **ULONG**

Um valor que especifica o tamanho de *pszName.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

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

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**SetName**](iuseridentity2-setname.md)
</dt> </dl>

 

 




