---
description: Não há suporte para GetOrdinal e podem ser alterados ou não disponíveis no futuro. Em vez disso, use Contas de Usuário com Troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: Método IUserIdentity2::GetOrdinal (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.GetOrdinal
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d5453a083a1db23e042d24c3da4cd2948ff70f813fcc9026a00324eade467918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968965"
---
# <a name="iuseridentity2getordinal-method"></a>Método IUserIdentity2::GetOrdinal

\[**Não há suporte para GetOrdinal** e podem ser alterados ou não disponíveis no futuro. Em vez disso, [use Contas de Usuário com a Opção de](fastuserswitching.md)Usuário Rápida e Área de Trabalho Remota .\]

Obtém o número ordinal dessa identidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwOrdinal* \[ out\]
</dt> <dd>

Tipo: **DWORD \***

Um ponteiro para um **valor DWORD** que recebe o número ordinal para essa identidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O ordinal determina a ordem das identidades na lista de identidade, mas pode não persistir em todas as operações nas identidades. Para obter um valor exclusivo para uma identidade, chame [**GetCookie**](iuseridentity-getcookie.md).

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**Getcookie**](iuseridentity-getcookie.md)
</dt> </dl>

 

 




