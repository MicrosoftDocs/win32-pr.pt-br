---
description: Define o parâmetro de direitos como um bitmap com cada bit correspondente a um direito de acesso.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Método GetCallerAccessRights da classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: c86ea3044411e33026ed6328fcfc227e615648b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796178"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a>Método GetCallerAccessRights da \_ \_ classe SystemSecurity

O método **\_ \_ SystemSecurity:: GetCallerAccessRights** define o parâmetro *Rights* como um bitmap com cada bit correspondente a um direito de acesso. Qualquer cliente pode chamá-lo para determinar quais direitos o cliente tem. Esse método é útil para clientes que habilitam ou desabilitam recursos. Por exemplo, um aplicativo de GUI pode desabilitar um botão se o usuário conectado no momento não tiver direitos de execução de método.

Qualquer cliente habilitado tem o direito de chamar **GetCallerAccessRights**, mesmo que esse cliente não tenha direitos de execução de método geral.

## <a name="syntax"></a>Sintaxe


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*direitos* \[ do fora\]
</dt> <dd>

Direitos de acesso do cliente. Para obter mais informações, consulte [**\_ \_ SystemSecurity**](--systemsecurity.md) and [WMI Security Constants](wmi-security-constants.md).

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ ENABLE** (1 (0x1))


</dt> <dd>

Habilita a conta e concede ao usuário permissões de leitura. Esse é o direito de acesso padrão para todos os usuários.

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ MÉTODO \_ Execute** (2 (0x2))


</dt> <dd>

Permite a execução de métodos.

> [!Note]  
> Os provedores podem executar verificações de acesso adicionais.

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ \_ \_ Rep. de gravação completa** (4 (0x4))


</dt> <dd>

Permite que o chamador, o contexto de segurança ou o usuário grave em classes e instâncias, exceto nas classes do sistema.

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ \_ \_ Representante de gravação parcial** (8 (0x8))


</dt> <dd>

Permite que o chamador, o contexto de segurança ou o usuário grave instâncias de provedor, mas não classes estáticas ou instâncias estáticas para o repositório.

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ \_Provedor de gravação** (16 (0x10))


</dt> <dd>

Permite que o chamador, o contexto de segurança ou o usuário grave classes e instâncias em provedores.

> [!Note]  
> A representação de provedores pode fazer verificações de acesso adicionais.

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ \_Acesso remoto** (32 (0x20))


</dt> <dd>

Permite que uma conta de usuário execute remotamente qualquer operação permitida pelas permissões definidas por outros bits.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Ler \_ CONTROLE** (131072 (0x20000))


</dt> <dd>

Permite o acesso de leitura aos descritores de segurança.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Gravar \_ DAC** (262144 (0x40000))


</dt> <dd>

Permite acesso de gravação para listas de controle de acesso discricional (DACL).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **HRESULT** que indica o status da chamada do método. A lista a seguir lista os valores de retorno que são de significância a [**Set9XUserList**](--systemsecurity-set9xuserlist.md). Para aplicativos de script e Visual Basic, o resultado pode ser obtido de [Parameters. ReturnValue](parsing-outparameters-objects.md). Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**\_método WBEM \_ E \_ desabilitado**
</dt> <dd>

Não há suporte para esse método em versões do Windows com suporte.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity:: Obtém-se**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity:: definido**](--systemsecurity-setsd.md)
</dt> <dt>

[Constantes de segurança do WMI](wmi-security-constants.md)
</dt> <dt>

[**Ace do Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Protegendo namespaces WMI](securing-wmi-namespaces.md)
</dt> <dt>

Constantes de segurança do WMI
</dt> </dl>

 

