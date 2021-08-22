---
description: Obtém o descritor de segurança que controla o acesso ao namespace WMI ao qual você está conectado. O descritor de segurança é retornado como uma instância de \_ \_ SecurityDescriptor.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: Método GetSecurityDescriptor da __SystemSecurity classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 77053174878db77409c525510acb54740ac8ad5c5c0505af5bf6ff8421cdf737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050854"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Método GetSecurityDescriptor da \_ \_ classe SystemSecurity

O **método GetSecurityDescriptor** obtém o descritor de segurança que controla o acesso ao namespace WMI ao qual você está conectado. O descritor de segurança é retornado como uma instância de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md). Para obter mais informações, consulte [Alterando a segurança de acesso em objetos securáveis.](changing-access-security-on-securable-objects.md)

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Descritor* \[ out\]
</dt> <dd>

O descritor de segurança associado ao namespace WMI.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro. Para obter mais informações, [consulte Códigos de retorno WMI](wmi-return-codes.md) ou [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**0**
</dt> <dd>

Conclusão bem-sucedida.

</dd> <dt>

**2**
</dt> <dd>

O usuário não tem acesso às informações solicitadas.

</dd> <dt>

**8**
</dt> <dd>

Falha desconhecida.

</dd> <dt>

**9**
</dt> <dd>

O usuário não tem privilégios adequados para executar o método.

</dd> <dt>

**21**
</dt> <dd>

Um parâmetro especificado na chamada de método não é válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

A [**instância \_ securityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL [*(lista*](/windows/desktop/SecGloss/d-gly) de controle de acesso discricionário) e uma SACL [*(lista*](/windows/desktop/SecGloss/s-gly) de controle de acesso do sistema). Para obter mais informações, consulte [Listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **o SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado. Para obter mais informações, consulte [**Constantes de privilégio**](privilege-constants.md) [e Executando operações privilegiadas](executing-privileged-operations.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[Definindo Descritores de Segurança namepace](setting-namespace-security-descriptors.md)
</dt> </dl>

 

