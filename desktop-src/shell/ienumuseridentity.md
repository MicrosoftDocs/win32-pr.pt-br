---
description: IEnumUserIdentity não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: Interface IEnumUserIdentity (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967888"
---
# <a name="ienumuseridentity-interface"></a>Interface IEnumUserIdentity

\[**IEnumUserIdentity** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Fornece a enumeração de todas as identidades de usuário presentes no sistema.

## <a name="members"></a>Membros

A interface **IEnumUserIdentity** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumUserIdentity** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumUserIdentity** tem esses métodos.



| Método                                         | Descrição                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**8i**](ienumuseridentity-clone.md)       | Preterido. Obtém uma cópia da enumeração atual.<br/>                                                               |
| [**GetCount**](ienumuseridentity-getcount.md) | Preterido. Obtém a contagem de identidades de usuário atualmente no sistema.<br/>                                            |
| [**Avançar**](ienumuseridentity-next.md)         | Preterido. Recupera uma matriz de interfaces de identidade do usuário da enumeração.<br/>                                  |
| [**Definido**](ienumuseridentity-reset.md)       | Preterido. Redefine a contagem interna de interfaces recuperadas na enumeração.<br/>                                 |
| [**Ignorar**](ienumuseridentity-skip.md)         | Preterido. Ignora um determinado número de interfaces de identidade de usuário na enumeração. Usado ao recuperar interfaces.<br/> |



 

## <a name="remarks"></a>Comentários

Para recuperar informações sobre as identidades de usuário presentes no sistema, você pode usar essa interface. Em uma interface [**IUserIdentityManager**](iuseridentitymanager.md) , você pode chamar [**IUserIdentityManager:: EnumIdentities**](iuseridentitymanager-enumidentities.md) para recuperar essa interface.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                  |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> </dl>

 

 
