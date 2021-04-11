---
title: Classe Win32_SessionDirectoryCluster
description: Fornece propriedades para exibir as propriedades de um farm no agente do Conexão de Área de Trabalho Remota (agente de conexão RD).
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionDirectoryCluster Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionDirectoryCluster classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3979dbe5403ca8f18e941b01e95774dabefe3211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454975"
---
# <a name="win32_sessiondirectorycluster-class"></a>\_Classe Win32 SessionDirectoryCluster

Fornece propriedades para exibir as propriedades de um farm no agente do Conexão de Área de Trabalho Remota (agente de conexão RD).

> [!Note]  
> No Windows Server 2008 R2, o nome do agente de sessão dos serviços de terminal (agente de Sessão TS) foi alterado para o agente de conexão RD. Essas propriedades se aplicam a todos os sistemas operacionais com suporte, salvo indicação em contrário.

 

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ SessionDirectoryCluster** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ SessionDirectoryCluster** tem essas propriedades.

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome do farm no agente de conexão RD.

</dd> <dt>

**NumberOfServers**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de servidores no farm no agente de conexão RD.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Modo de sessão única do farm no agente de conexão RD.

<dt>

0
</dt> <dd>

O farm no agente de conexão de área de trabalho remota não está no modo de sessão única.

</dd> <dt>

1
</dt> <dd>

O farm no agente de conexão de área de trabalho remota está em modo de sessão única.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SessionDirectoryServer Win32**](win32-sessiondirectoryserver.md)
</dt> <dt>

[**\_SessionDirectorySession Win32**](win32-sessiondirectorysession.md)
</dt> </dl>

 

