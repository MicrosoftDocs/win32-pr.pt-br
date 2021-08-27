---
description: Remove um sistema de computador de um domínio ou grupo de trabalho.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Método UnjoinDomainOrWorkgroup da Win32_ComputerSystem classe
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
ms.openlocfilehash: 992aa6c84f912f705e02252d1ac6d24422934edb991c049de188ab5fb0ccbfa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105066"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Método UnjoinDomainOrWorkgroup da classe \_ ComputerSystem Win32

O **método UnjoinDomainOrWorkgroup** remove um sistema de computador de um domínio ou grupo de trabalho.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

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

*Senha* \[ Em\]
</dt> <dd>

Se o *parâmetro UserName* especificar um nome de conta, o parâmetro *Password* deverá apontar para a senha a ser usada ao se conectar ao controlador de domínio. Caso contrário, esse parâmetro deve ser **NULL.**

> [!Note]  
>  A senha deve usar um alto nível de autenticação, não menor que **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**, ao se conectar ao Winmgmt ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) no ponteiro [**IWbemServices.**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) Se for local para Winmgmt, isso não será uma preocupação.

 

</dd> <dt>

*UserName* \[ Em\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres com terminação nula constante que especifica o nome da conta a ser usado ao se conectar ao controlador de domínio. Deve especificar um domínio e uma conta de usuário, por exemplo, "usuário \\ de domínio" ou user@domain " ". Se esse parâmetro for **NULL,** o contexto do chamador será usado.

> [!Note]  
> *UserName* deve usar um alto nível de autenticação, não menos que **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**, ao se conectar ao Winmgmt ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) no ponteiro [**IWbemServices.**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) Se for local para Winmgmt, isso não será uma preocupação.

 

</dd> <dt>

*FUnjoinOptions* \[ Em\]
</dt> <dd>

Conjunto de sinalizadores de bits que definem as opções de desajoso.

<dt>



  acima (0)


</dt> <dd>

Padrão. Não há opções.

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP \_ ACCT \_ DELETE** (4)


</dt> <dd>

Desabilite a conta do Active Directory após a operação de desajoso, mas não exclua a conta.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

O **método UnjoinDomainOrWorkgroup** retorna 0 (zero) em caso de êxito ou quando nenhuma opção está envolvida. Qualquer outro valor indica um erro. Para códigos de erro, [**consulte Constantes de**](/windows/desktop/WmiSdk/wmi-error-constants) erro WMI ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Outros** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

Depois de chamar esse método, reinicie o computador afetado para aplicar as alterações.

## <a name="examples"></a>Exemplos

[O desaconsinar um computador de um domínio](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) O exemplo de VBScript desaconscria o computador local de seu domínio atual e desabilita a conta de computador.

O [exemplo Desaconsinar um Computador de](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) um Domínio usando script VBS desaconsinte um computador especificado de um domínio. .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ ComputerSystem**](win32-computersystem.md)
</dt> <dt>

[**Método JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

