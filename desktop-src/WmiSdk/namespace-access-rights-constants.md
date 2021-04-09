---
description: 'O WMI tem constantes de segurança usadas para verificação de acesso de namespace por \_ \_ SystemSecurity:: GetCallerAccessRights.'
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Constantes de direitos de acesso de namespace (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 469e036b7cd385fa2ac2bae23e0da081288b536b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010346"
---
# <a name="namespace-access-rights-constants"></a>Constantes de direitos de acesso de namespace

O WMI tem constantes de segurança usadas para verificação de acesso de namespace por [**\_ \_ SystemSecurity:: GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md). Para obter informações de segurança sobre listas de controle de acesso (ACLs, DACLs ou SACLs), consulte [listas de controle de acesso (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) e [**direitos de acesso padrão**](/windows/desktop/SecAuthZ/standard-access-rights). Essas constantes são definidas na enumeração **\_ \_ flags de segurança do WBEM** .

<dl> <dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**habilitar o WBEM \_**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Habilita a conta e concede ao usuário permissões de leitura. Esse é um direito de acesso padrão para todos os usuários e corresponde à permissão habilitar conta na guia Segurança do [*controle WMI*](gloss-w.md). Para obter mais informações, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).


</dt> </dl> </dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**\_execução do método WBEM \_**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Permite a execução de métodos. Os provedores podem executar verificações de acesso adicionais. Esse é um direito de acesso padrão para todos os usuários e corresponde à permissão execute Methods na guia Security do controle WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**\_representante de \_ gravação \_ completa do WBEM**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Permite que uma conta de usuário grave em classes no repositório do WMI, bem como em instâncias. Um usuário não pode gravar em classes do sistema. Somente os membros do grupo Administradores têm essa permissão. **WBEM \_ O \_ \_ representante de gravação completa** corresponde à permissão de gravação completa na guia Segurança do controle WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**\_representante de \_ gravação \_ parcial do WBEM**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Permite que você grave dados somente em instâncias, não em classes. Um usuário não pode gravar classes no [*repositório do WMI*](gloss-w.md). Somente os membros do grupo Administradores têm esse direito. **WBEM \_ O \_ \_ representante de gravação parcial** corresponde à permissão de gravação parcial na guia Segurança do controle WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**\_provedor de gravação WBEM \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Permite gravar classes e instâncias em provedores. Observe que os provedores podem realizar verificações de acesso adicionais ao representar um usuário. Esse é um direito de acesso padrão para todos os usuários e corresponde à permissão de gravação do provedor na guia Segurança do controle WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**\_acesso remoto \_ WBEM**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Permite que uma conta de usuário execute remotamente qualquer operação permitida pelas permissões descritas acima. Somente os membros do grupo Administradores têm esse direito. **WBEM \_ O \_ acesso remoto** corresponde à permissão habilitar remota na guia Segurança do controle WMI.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Wbemcli. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de segurança do WMI](wmi-security-constants.md)
</dt> <dt>

[Protegendo namespaces WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Acesso a namespaces WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

