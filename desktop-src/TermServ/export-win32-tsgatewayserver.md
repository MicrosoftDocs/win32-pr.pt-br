---
title: Método Export da classe Win32_TSGatewayServer
description: Retorna a configuração do servidor do gateway de Área de Trabalho Remota (Gateway RD) como uma cadeia de caracteres XML.
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de exportação
- Método de exportação Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServer
- Classe de Win32_TSGatewayServer Serviços de Área de Trabalho Remota, método de exportação
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919211"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a>Método Export da classe Win32 \_ TSGatewayServer

Retorna a configuração do servidor do gateway de Área de Trabalho Remota (Gateway RD) como uma cadeia de caracteres XML.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ExportType* \[ no\]
</dt> <dd>

O conteúdo a ser exportado. Defina o tipo de exportação definindo os bits correspondentes no parâmetro *ExportType* . Você pode definir vários tipos de exportação. Por exemplo, se o 0 bit for definido, Serviços de Área de Trabalho Remota RD CAPs (políticas de autorização de conexão) serão exportadas. Se 0 e o 2º bit forem definidos, as RD CAPs Serviços de Área de Trabalho Remota e as RD RAPs (políticas de autorização de recursos) serão exportadas.

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Exportar todas as tampas** (1)


</dt> <dd>

Exportar todas as RD CAPs.

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Exportar todos os servidores RADIUS** (2)


</dt> <dd>

Exportar uma lista de todos os servidores de servidor de diretivas de rede (NPS).

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Exportar todas as raps** (4)


</dt> <dd>

Exportar todas as RD RAPs.

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Exportar todos os RGS** (8)


</dt> <dd>

Exportar todos os grupos de recursos.

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Exportar todos os servidores de balanceamento de carga** (16)


</dt> <dd>

Exportar uma lista de todos os servidores de balanceamento de carga.

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Exportar todas as configurações do servidor** (32)


</dt> <dd>

Exportar todas as configurações de servidor relacionadas ao gateway de área de trabalho remota.

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Exportar todas as políticas de integridade** (64)


</dt> <dd>

Exportar todas as políticas de integridade.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: * *

Não há suporte para esse valor antes do Windows Server 2016.

</dd> </dl> </dd> <dt>

*XmlString* \[ fora\]
</dt> <dd>

A cadeia de caracteres XML.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGatewayServer Win32**](win32-tsgatewayserver.md)
</dt> </dl>

 

