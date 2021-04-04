---
title: Classe Win32_SessionDirectoryServer
description: Fornece propriedades para exibir as propriedades de um servidor do Conexão de Área de Trabalho Remota Broker (agente de conexão RD).
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionDirectoryServer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionDirectoryServer classe, descrita
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
ms.openlocfilehash: b9e96efb19e4db56e582cd44d05f3e9865e5282c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918306"
---
# <a name="win32_sessiondirectoryserver-class"></a>\_Classe Win32 SessionDirectoryServer

Fornece propriedades para exibir as propriedades de um servidor do Conexão de Área de Trabalho Remota Broker (agente de conexão RD).

> [!Note]  
> No Windows Server 2008 R2, o nome do agente de sessão dos serviços de terminal (agente de Sessão TS) foi alterado para o agente de conexão RD. Essas propriedades se aplicam a todos os sistemas operacionais com suporte, salvo indicação em contrário.

 

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

A classe **Win32 \_ SessionDirectoryServer** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ SessionDirectoryServer** tem essas propriedades.

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do farm que inclui o servidor.

</dd> <dt>

**Indicador**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um número relativo que representa a carga do Host da Sessão RD Server quando o algoritmo de balanceamento de carga padrão é usado. O valor da propriedade *loadindicator* é baseado no número de sessões, no número de solicitações de redirecionamento pendentes e no valor de peso do servidor.

</dd> <dt>

**NumberOfSessions**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de sessões no servidor do agente de conexão de área de trabalho remota.

</dd> <dt>

**NumPendRedir**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
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

Endereço IP do servidor do agente de conexão de área de trabalho remota. Se o servidor estiver configurado para endereços IPv4 e IPv6, ele conterá o endereço IPv4.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome do servidor do agente de conexão de área de trabalho remota.

</dd> <dt>

**ServerWeight**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor de peso do servidor, usado no balanceamento de carga.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Configuração de modo de sessão única do servidor do agente de conexão RD.

<dt>

0
</dt> <dd>

O farm não está no modo de sessão única.

</dd> <dt>

1
</dt> <dd>

O farm no está em modo de sessão única.

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

[**\_SessionDirectoryCluster Win32**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**\_SessionDirectorySession Win32**](win32-sessiondirectorysession.md)
</dt> </dl>

 

