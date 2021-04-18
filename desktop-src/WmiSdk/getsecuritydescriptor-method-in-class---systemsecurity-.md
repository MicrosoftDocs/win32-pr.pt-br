---
description: Obtém o descritor de segurança que controla o acesso ao namespace do WMI ao qual você está conectado. O descritor de segurança é retornado como uma instância de \_ \_ SecurityDescriptor.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: Método GetSecurityDescriptor da classe __SystemSecurity
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
ms.openlocfilehash: 7aece0a50678689141de9b9a38a014414578de3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765684"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Método GetSecurityDescriptor da \_ \_ classe SystemSecurity

O método **GetSecurityDescriptor** Obtém o descritor de segurança que controla o acesso ao namespace do WMI ao qual você está conectado. O descritor de segurança é retornado como uma instância de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md). Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Descritor* \[ fora\]
</dt> <dd>

O descritor de segurança associado ao namespace WMI.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro. Para obter mais informações, consulte [códigos de retorno do WMI](wmi-return-codes.md) ou [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).

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

**Abril**
</dt> <dd>

Um parâmetro especificado na chamada do método não é válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema. Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado. Para obter mais informações, consulte [**constantes de privilégio**](privilege-constants.md) e [executando operações privilegiadas](executing-privileged-operations.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> </dl>

 

