---
title: Win32_SessionDirectoryVMMPlugin classe
description: Representa um plug-in do VMM (Virtual Machine Manager) registrado com um agente de sessão.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVMMPlugin classe Serviços de Área de Trabalho Remota
- Win32_SessionDirectoryVMMPlugin classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7481022951664b49b912b854e96e2d30895b0716ee67b6eb01ce1a9f1b1561ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422356"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a>Classe \_ SessionDirectoryVMMPlugin do Win32

Representa um plug-in do VMM (Virtual Machine Manager) registrado com um agente de sessão.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a>Membros

A **classe \_ SessionDirectoryVMMPlugin do Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ SessionDirectoryVMMPlugin do Win32** tem esses métodos.



| Método                                                                             | Descrição                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetCurrentVMMPlugin**](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | Obtém o plug-in de prioridade mais alta habilitado.<br/> |
| [**RegisterVMMPlugin**](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | Registra um novo plug-in do VMM.<br/>                       |
| [**Setenabled**](setenabled-win32-sessiondirectoryvmmplugin.md)                   | Habilita ou desabilita o plug-in.<br/>                   |
| [**SetName**](setname-win32-sessiondirectoryvmmplugin.md)                         | Define o nome do plug-in.<br/>                      |
| [**Setpriority**](setpriority-win32-sessiondirectoryvmmplugin.md)                 | Define a prioridade do plug-in.<br/>                  |
| [**SetProvider**](setprovider-win32-sessiondirectoryvmmplugin.md)                 | Define o nome do provedor do plug-in.<br/>             |
| [**SetServiceLocation**](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | Define o local de serviço do plug-in.<br/>          |
| [**UnregisterVMMPlugin**](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | Não registrou o plug-in.<br/>                           |



 

### <a name="properties"></a>Propriedades

A **classe \_ SessionDirectoryVMMPlugin do Win32** tem essas propriedades.

<dl> <dt>

**Habilitada**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o plug-in está habilitado ou desabilitado. **True** se o plug-in estiver habilitado ou **false** caso contrário. O plug-in está desabilitado por padrão.

</dd> <dt>

**Prioridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

A prioridade do plug-in. Quanto maior o valor, maior a prioridade do plug-in. A prioridade é zero por padrão.

</dd> <dt>

**sClassID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O identificador de classe do plug-in.

</dd> <dt>

**sName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do plug-in.

</dd> <dt>

**sProvider**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do provedor de plug-in.

</dd> <dt>

**sServiceLocation**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O local de serviço que o plug-in deve contatar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

