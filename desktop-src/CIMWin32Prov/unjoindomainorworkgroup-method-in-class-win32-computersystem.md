---
description: Remove um sistema de computador de um domínio ou grupo de trabalho.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Método UnjoinDomainOrWorkgroup da classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826630"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Método UnjoinDomainOrWorkgroup da classe Win32 \_ ComputerSystem

O método **UnjoinDomainOrWorkgroup** remove um sistema de computador de um domínio ou grupo de trabalho.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Senha* \[ do no\]
</dt> <dd>

Se o parâmetro *username* especificar um nome de conta, o parâmetro *password* deverá apontar para a senha a ser usada na conexão com o controlador de domínio. Caso contrário, esse parâmetro deve ser **nulo**.

> [!Note]  
> A *senha* deve usar um nível de autenticação alto, não menor que a privacidade do PCT de **\_ \_ \_ nível \_ \_ de autenticação RPC C**, ao se conectar a winmgmt ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) no ponteiro de [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) . Se for local para winmgmt, isso não é uma preocupação.

 

</dd> <dt>

*Nome de usuário* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres constante terminada em nulo que especifica o nome da conta a ser usada ao conectar-se ao controlador de domínio. É necessário especificar uma conta de domínio e de usuário, por exemplo, "domínio \\ usuário" ou " user@domain ". Se esse parâmetro for **NULL**, o contexto do chamador será usado.

> [!Note]  
> O *nome de usuário* deve usar um nível de autenticação alto, não menor que a privacidade do PCT de **\_ \_ \_ nível \_ \_ de autenticação RPC C**, ao se conectar a winmgmt ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) no ponteiro de [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) . Se for local para winmgmt, isso não é uma preocupação.

 

</dd> <dt>

*FUnjoinOptions* \[ no\]
</dt> <dd>

Conjunto de sinalizadores de bits que definem as opções de desjunção.

<dt>



  acima (0)


</dt> <dd>

Padrão. Não há opções.

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>INSTALAÇÃO do NET **\_ \_Exclusão de acct** (4)


</dt> <dd>

Desabilite a conta de Active Directory após a operação de desassociação, mas não exclua a conta.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

O método **UnjoinDomainOrWorkgroup** retorna 0 (zero) em caso de êxito ou quando não há opções envolvidas. Qualquer outro valor indica um erro. Para códigos de erro, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Outro** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

Depois de chamar esse método, reinicie o computador afetado para aplicar as alterações.

## <a name="examples"></a>Exemplos

[A desassociação de um computador de um domínio](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) A amostra do VBScript desune o computador local do seu domínio atual e desabilita a conta do computador.

O exemplo [desassociar um computador de um domínio usando script vbs](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) não une um computador especificado de um domínio. .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Sistema de ComputerSystem Win32**](win32-computersystem.md)
</dt> <dt>

[**Método JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

