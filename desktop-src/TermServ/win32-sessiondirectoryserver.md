---
title: Win32_SessionDirectoryServer classe
description: Fornece propriedades para exibir as propriedades de um Conexão de Área de Trabalho Remota Broker (Agente de Conexão de Área de Trabalho Remota).
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryServer classe Serviços de Área de Trabalho Remota
- Win32_SessionDirectoryServer classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702b56a9cf8aee2ab38ad9d6b3a0f2d270b2128ea46934cc1beb720c77400d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127066"
---
# <a name="win32_sessiondirectoryserver-class"></a>Classe \_ SessionDirectoryServer do Win32

Fornece propriedades para exibir as propriedades de um Conexão de Área de Trabalho Remota Broker (Agente de Conexão de Área de Trabalho Remota).

> [!Note]  
> No Windows Server 2008 R2, o nome do Agente de Sessão dos Serviços de Terminal (Agente de Sessão TS) foi alterado para Agente de Conexão de Área de Trabalho Remoto. Essas propriedades se aplicam a todos os sistemas operacionais com suporte, a menos que seja notado de outra forma.

 

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a>Membros

A **classe \_ SessionDirectoryServer do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ SessionDirectoryServer do Win32** tem essas propriedades.

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do farm que inclui o servidor.

</dd> <dt>

**LoadIndicator**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um número relativo que representa a Host da Sessão RD do servidor quando o algoritmo de balanceamento de carga padrão é usado. O *valor da propriedade LoadIndicator* baseia-se no número de sessões, no número de solicitações de redirecionamento pendentes e no valor de peso do servidor.

</dd> <dt>

**NumberOfSessions**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de sessões no servidor do Agente de Conexão de Área de Trabalho Local.

</dd> <dt>

**NumPendRedir**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de solicitações de redirecionamento pendentes.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereço IP do servidor do Agente de Conexão de RD. Se o servidor estiver configurado para endereços IPv4 e IPv6, ele conterá o endereço IPv4.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome do servidor do Agente de Conexão de RD.

</dd> <dt>

**ServerWeight**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor de peso do servidor, usado no balanceamento de carga.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Configuração de modo de sessão única do servidor do Agente de Conexão de RD.

<dt>

0
</dt> <dd>

O farm não está no modo de sessão única.

</dd> <dt>

1
</dt> <dd>

O farm em está no modo de sessão única.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ SessionDirectoryCluster**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**SessionDirectorySession do Win32 \_**](win32-sessiondirectorysession.md)
</dt> </dl>

 

