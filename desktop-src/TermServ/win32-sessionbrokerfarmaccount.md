---
title: Win32_SessionBrokerFarmAccount classe
description: A classe SessionBrokerFarmAccount do Win32 não está mais disponível para uso \_ desde Windows Server 2012. | Win32_SessionBrokerFarmAccount classe
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarmAccount classe Serviços de Área de Trabalho Remota
- Win32_SessionBrokerFarmAccount classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b7d55f973dc19c03182a4199b64f91f9de5a0774cc8c8f9d77d67eeb715c24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422486"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a>Classe \_ SessionBrokerFarmAccount do Win32

\[A **classe \_ SessionBrokerFarmAccount do Win32** não está mais disponível para uso desde Windows Server 2012.\]

Define uma conta de farm do agente de sessão.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a>Membros

A **classe \_ SessionBrokerFarmAccount do Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ SessionBrokerFarmAccount do Win32** tem esses métodos.



| Método                                                      | Descrição                          |
|:------------------------------------------------------------|:-------------------------------------|
| [**DeleteEx**](deleteex-win32-sessionbrokerfarmaccount.md) | Exclui a conta do farm.<br/> |



 

### <a name="properties"></a>Propriedades

A **classe \_ SessionBrokerFarmAccount do Win32** tem essas propriedades.

<dl> <dt>

**AccountDomain**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O nome do domínio ao que a conta do farm pertence.

</dd> <dt>

**AccountName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O nome da conta do farm.

</dd> <dt>

**AccountPassword**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

A senha da conta do farm.

</dd> <dt>

**AccountSPN1**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O primeiro SPN (nome da entidade de serviço) associado à conta do farm.

</dd> <dt>

**AccountSPN2**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O segundo SPN associado à conta do farm.

</dd> <dt>

**ComputerDNSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O nome DNS do computador associado à conta do farm.

</dd> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O nome do farm do agente de sessão.

</dd> <dt>

**Manual**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica se a senha da conta é atualizada manualmente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Fim do suporte ao cliente<br/>    | Nenhum compatível<br/>                                                              |
| Fim do suporte ao servidor<br/>    | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

