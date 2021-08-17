---
title: Classe Win32_TSVirtualDesktopServerSettings
description: Contém informações de configuração para um servidor de Host de Virtualização de Área de Trabalho Remota (host de Virtualização RD).
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSVirtualDesktopServerSettings Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSVirtualDesktopServerSettings classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40e7d51ee0c92e50afca023629bb92de9f506b3e47ee9e520aa16c09640375b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137459"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a>\_Classe Win32 TSVirtualDesktopServerSettings

Contém informações de configuração para um servidor de Host de Virtualização de Área de Trabalho Remota (host de Virtualização RD).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSVirtualDesktopServerSettings** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSVirtualDesktopServerSettings** tem essas propriedades.

<dl> <dt>

**Simultaneidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O máximo permitido de solicitações simultâneas de provisionamento para este servidor de área de trabalho virtual.

</dd> <dt>

**PolicySourceSessionBrokerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se definido como 0, indica que a propriedade **SessionBrokerName** está configurada pelo servidor; Se definido como 1, indica que a propriedade **SessionBrokerName** é configurada por uma política de grupo.

</dd> <dt>

**SessionBrokerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O nome distinto totalmente qualificado do agente de sessão para o servidor de host de virtualização de área de trabalho remota.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | \\TerminalServices da cimv2 raiz \\<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





