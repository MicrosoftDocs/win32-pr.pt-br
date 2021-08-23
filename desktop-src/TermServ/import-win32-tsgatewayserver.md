---
title: Método de importação da Win32_TSGatewayServer classe
description: Importa uma determinada configuração para o servidor Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Importar o método Serviços de Área de Trabalho Remota
- Classe Serviços de Área de Trabalho Remota , Win32_TSGatewayServer importação
- Win32_TSGatewayServer classe Serviços de Área de Trabalho Remota , método Import
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
ms.openlocfilehash: 2629e8e44acd0f617e86a846cc127ab77250673c8612f2d2f53ab8c0238d9f0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574566"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a>Método de importação da \_ classe TSGatewayServer do Win32

Importa uma determinada configuração para o servidor Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).

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

*ImportType* \[ Em\]
</dt> <dd>

O conteúdo a ser importado. De definir o tipo de importação definindo os bits correspondentes no *parâmetro ImportType.* Você pode definir vários tipos de importação. Por exemplo, se o 0 bit estiver definido, Serviços de Área de Trabalho Remota de autorização de conexão (CAPs de RD) serão importadas. Se o 0 e o 2º bit estão definidos, os CAPs de RD e Serviços de Área de Trabalho Remota RAPs (políticas de autorização de recursos de RD) serão importados.

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Importar todos os CAPs** (1)


</dt> <dd>

Importe todos os CAPs de RD.

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Importar todos os servidores Radius** (2)


</dt> <dd>

Importe uma lista de todos os servidores NPS (Servidor de Políticas de Rede).

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Importar todos os RAPs** (4)


</dt> <dd>

Importe todos os RAPs de RD.

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Importar todos os RGs** (8)


</dt> <dd>

Importe todos os grupos de recursos.

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Importar todos os servidores LoadBalancing** (16)


</dt> <dd>

Importe uma lista de todos os servidores de balanceamento de carga.

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Importar todos os servidores Configurações** (32)


</dt> <dd>

Importe todas as configurações de servidor relacionadas ao Gateway de Área de Trabalho Local.

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Importar todas as Políticas de Saúde** (64)


</dt> <dd>

Importe todas as políticas de saúde.

**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: **

Esse valor não é suportado antes Windows Server 2016.

</dd> </dl> </dd> <dt>

*XmlString* \[ Em\]
</dt> <dd>

A configuração como uma cadeia de caracteres XML.

</dd> <dt>

*MergeOrReplace* \[ Em\]
</dt> <dd>

Indica se os dados devem ser mesclados ou substituídos quando ocorre um conflito.

> [!Note]  
> A mesclagem ainda não foi implementada. Portanto, esse valor de parâmetro é ignorado.

 

</dd> <dt>

*LogString* \[ out\]
</dt> <dd>

As informações de log geradas durante a operação de importação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSGatewayServer**](win32-tsgatewayserver.md)
</dt> </dl>

 

