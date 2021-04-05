---
title: Classe Win32_SessionBrokerTarget
description: Define a consulta para um destino de agente de sessão.
ms.assetid: 35de25da-cb89-4836-be14-9544b1264248
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionBrokerTarget Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionBrokerTarget classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTarget
- Win32_SessionBrokerTarget.PluginName
- Win32_SessionBrokerTarget.TargetName
- Win32_SessionBrokerTarget.FarmName
- Win32_SessionBrokerTarget.Guid
- Win32_SessionBrokerTarget.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ceca0df64eeb9cd285737fee7c6ca6fa3a2e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824773"
---
# <a name="win32_sessionbrokertarget-class"></a>\_Classe Win32 SessionBrokerTarget

Define a consulta para um destino de agente de sessão.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERTARGET_Prov"), AMENDMENT]
class Win32_SessionBrokerTarget
{
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ SessionBrokerTarget** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ SessionBrokerTarget** tem essas propriedades.

<dl> <dt>

**Ambiente**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do ambiente. No caso de um destino de máquina virtual (VM), esse pode ser o nome do host da VM.

</dd> <dt>

**Farmname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do farm ao qual o destino pertence.

</dd> <dt>

**Volume**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O GUID (se houver) do destino.

</dd> <dt>

**PluginName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O nome do plug-in.

</dd> <dt>

**TargetName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do destino.

</dd> </dl>

## <a name="examples"></a>Exemplos

A cadeia de caracteres de consulta a seguir demonstra como a \_ classe SessionBrokerTarget do Win32 é usada em uma consulta.


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerTarget WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

