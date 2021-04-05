---
title: Método de importação da classe Win32_TSGatewayServer
description: Importa uma determinada configuração para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Método de importação Serviços de Área de Trabalho Remota
- Método de importação Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServer
- Classe de Win32_TSGatewayServer Serviços de Área de Trabalho Remota, método de importação
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b35395342be7c13f2a96f73f914eda103e1ef4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918659"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a>Método de importação da \_ classe Win32 TSGatewayServer

Importa uma determinada configuração para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ImportType* \[ no\]
</dt> <dd>

O conteúdo a ser importado. Defina o tipo de importação definindo os bits correspondentes no parâmetro *importType* . Você pode definir vários tipos de importação. Por exemplo, se o 0 bit for definido, Serviços de Área de Trabalho Remota RD CAPs (políticas de autorização de conexão) serão importadas. Se 0 e o 2º bit forem definidos, as RD CAPs Serviços de Área de Trabalho Remota e as RD RAPs (políticas de autorização de recursos) serão importadas.

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Importar todas as tampas** (1)


</dt> <dd>

Importar todas as RD CAPs.

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Importar todos os servidores RADIUS** (2)


</dt> <dd>

Importe uma lista de todos os servidores de servidor de diretivas de rede (NPS).

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Importar todas as raps** (4)


</dt> <dd>

Importar todas as RD RAPs.

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Importar todos os RGS** (8)


</dt> <dd>

Importar todos os grupos de recursos.

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Importar todos os servidores de balanceamento de carga** (16)


</dt> <dd>

Importe uma lista de todos os servidores de balanceamento de carga.

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Importar todas as configurações do servidor** (32)


</dt> <dd>

Importar todas as configurações de servidor relacionadas ao gateway de área de trabalho remota.

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Importar todas as políticas de integridade** (64)


</dt> <dd>

Importar todas as políticas de integridade.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: * *

Não há suporte para esse valor antes do Windows Server 2016.

</dd> </dl> </dd> <dt>

*XmlString* \[ no\]
</dt> <dd>

A configuração como uma cadeia de caracteres XML.

</dd> <dt>

*MergeOrReplace* \[ no\]
</dt> <dd>

Indica se os dados devem ser mesclados ou substituídos quando ocorre um conflito.

> [!Note]  
> A mesclagem ainda não foi implementada. Portanto, esse valor de parâmetro é ignorado.

 

</dd> <dt>

*LogString* \[ fora\]
</dt> <dd>

As informações de log geradas durante a operação de importação.

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

 

