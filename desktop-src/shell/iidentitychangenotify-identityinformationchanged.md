---
description: IdentityInformationChanged não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: 3aca8a98-3d12-482d-9991-d6b53adde522
title: 'Método IIdentityChangeNotify:: IdentityInformationChanged (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.IdentityInformationChanged
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: c33f67a4def3312564ed943e2a3a917fe2843980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828281"
---
# <a name="iidentitychangenotifyidentityinformationchanged-method"></a>Método IIdentityChangeNotify:: IdentityInformationChanged

\[**IdentityInformationChanged** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Chamado quando informações sobre uma identidade de usuário são alteradas ou quando uma identidade de usuário é adicionada ou excluída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IdentityInformationChanged(
   DWORD dwType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwType* 
</dt> <dd>

Tipo: **DWORD**

Um valor que especifica o tipo de informação alterado ou a operação executada em uma identidade. Pode ser uma combinação dos valores a seguir.

<dt>



 (IIC \_ \_identidade atual \_ alterada)


</dt> <dd>

A identidade atual foi modificada.

</dd> <dt>



 (IIC \_ IDENTIDADE \_ alterada)


</dt> <dd>

Uma identidade foi modificada.

</dd> <dt>



 (IIC \_ IDENTIDADE \_ excluída)


</dt> <dd>

Uma identidade foi excluída.

</dd> <dt>



 (IIC \_ IDENTIDADE \_ adicionada)


</dt> <dd>

Uma nova identidade foi adicionada.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Você pode implementar esse método para fornecer um comportamento personalizado para seu aplicativo quando a lista de identidades de usuário no sistema tiver sido modificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fim do suporte do servidor<br/>    | Windows 2000 Server<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



 

 




