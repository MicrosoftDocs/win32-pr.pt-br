---
title: Classe Win32_SessionBrokerServiceProperties
description: Define a consulta para um serviço de agente de sessão.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionBrokerServiceProperties Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionBrokerServiceProperties classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499775"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a>\_Classe Win32 SessionBrokerServiceProperties

Define a consulta para um serviço de agente de sessão.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ SessionBrokerServiceProperties** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](/windows)

### <a name="methods"></a>Métodos

A classe **Win32 \_ SessionBrokerServiceProperties** tem esses métodos.



| Método                                                                                                | Descrição                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteSBDbConnectionString**](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | Exclui cadeias de conexão de BD (primária e secundária) do registro.<br/> **Windows server 2012 R2, Windows server 2012 e Windows server 2008 R2:** Este método não está disponível antes do Windows Server 2016<br/> |
| [**InstallBrokerDatabase**](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | Instala o BD do agente de conexão RD no SQL Server central<br/>                                                                                                                                                                    |
| [**IsDbReachable**](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | Verifica se o BD está acessível<br/>                                                                                                                                                                                                 |
| [**SetBrokerHAMode**](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | Migra dados do BD de WID local para o novo SQL Server DB baseado. Ele também configura o servidor do agente para usar o SQL Server central<br/>                                                                                        |
| [**SetBrokerNonHAMode**](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | Migra dados do SQL Server central para o local DB. Ele também configura o servidor do agente para usar o BD local.<br/>                                                                                                              |
| [**SetSBDbConnectionStrings**](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | Salva as cadeias de conexão do BD (primária e secundária) no registro.<br/> **Windows server 2012 R2, Windows server 2012 e Windows server 2008 R2:** Este método não está disponível antes do Windows Server 2016<br/>     |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ SessionBrokerServiceProperties** tem essas propriedades.

<dl> <dt>

**SBDbConnectionString**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Cadeia de conexão de banco de dados usada pelo serviço de agente de sessão.

**Windows Server 2008 R2:** Essa propriedade não está disponível antes do Windows Server 2012

</dd> <dt>

**SBDbSecondaryConnectionString**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Opcional. Cadeia de conexão de banco de dados secundária usada pelo serviço de agente de sessão para dar suporte à expiração da senha.

**Windows server 2012 R2, Windows server 2012 e Windows server 2008 R2:** Essa propriedade não está disponível antes do Windows Server 2016

</dd> <dt>

**SBNetworkName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome de rede usado pelo serviço de agente de sessão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

