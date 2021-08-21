---
description: Grava uma versão atualizada do descritor de segurança que controla o acesso ao namespace WMI ao qual você está conectado. O descritor de segurança é representado por uma instância de \_ \_ SecurityDescriptor.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: Método SetSecurityDescriptor da __SystemSecurity classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d44322820514fc676c1b3ad304375f5f3ce8966a73217c6505f24659914f7853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315623"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a>Método SetSecurityDescriptor da \_ \_ classe SystemSecurity

O [**método SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) grava uma versão atualizada do descritor de segurança que controla o acesso ao namespace WMI ao qual você está conectado. O descritor de segurança é representado por uma instância de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md). Para obter mais informações, consulte [Alterando a segurança de acesso em objetos securáveis.](changing-access-security-on-securable-objects.md)

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Descritor* \[ Em\]
</dt> <dd>

O descritor de segurança associado ao Namespace WMI.

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

A [**instância \_ securityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL [*(lista*](/windows/desktop/SecGloss/d-gly) de controle de acesso discricionário) e uma SACL [*(Lista*](/windows/desktop/SecGloss/a-gly) de Controle de Acesso do Sistema). Para obter mais informações, consulte [Listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **o SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado. Para obter mais informações, consulte [**Constantes de privilégio**](privilege-constants.md) [e Executando operações privilegiadas](executing-privileged-operations.md).

Você pode atualizar a DACL e a SACL na instância [**\_ do Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ao chamar esse método, mas também pode atualizar apenas a DACL ou apenas a SACL.

Os valores a seguir [**em SECURITY \_ DESCRIPTOR \_ CONTROL determinam**](/windows/desktop/SecAuthZ/security-descriptor-control) se a DACL ou a SACL ou ambas são atualizadas.

-   **\_ES DACL \_ PRESENT**

    Indica que a DACL deve ser atualizada. Se isso não for definido, o WMI preservará o valor original da DACL.

-   **\_ES SACL \_ PRESENT**

    Indica que a SACL deve ser atualizada. Se isso não for definido, o WMI preservará o valor original da SACL. Para atualizar a SACL, a conta deve ter o privilégio **SeSecurityPrivilege** habilitado. Para scripts, o nome do privilégio **é SeSecurityPrivilege.** Para obter mais informações, consulte [**Constantes de privilégio**](privilege-constants.md).

Se as propriedades do usuário confiável grupo e proprietário não são **NULL,** elas são atualizadas. Caso contrário, o WMI preservará os valores originais. Para obter mais informações, consulte [Objetos do descritor de](wmi-security-descriptor-objects.md)segurança WMI .

Quando uma nova SACL é **NULL** em uma chamada a esse método, o SACL descritor de segurança no objeto passível de proteger de destino é deixado inalterado.

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

 

