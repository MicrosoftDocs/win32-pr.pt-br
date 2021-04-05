---
title: Método SetBrokerHAMode da classe Win32_SessionBrokerServiceProperties
description: Migra os dados de um banco de dado de WID local para o novo banco de dados baseado em SQL Server. Ele também configura o servidor do agente para usar o SQL Server central.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetBrokerHAMode
- Método SetBrokerHAMode Serviços de Área de Trabalho Remota, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Serviços de Área de Trabalho Remota, método SetBrokerHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085553"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método SetBrokerHAMode da classe Win32 \_ SessionBrokerServiceProperties

Migra os dados de um banco de dado de WID local para o novo banco de dados baseado em SQL Server. Ele também configura o servidor do agente para usar o SQL Server central.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*connStringToCentralDBRdcms* \[ no\]
</dt> <dd>

Cadeia de conexão para o banco de dados central.

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[ no\]
</dt> <dd>

Cadeia de conexão secundária para o banco de dados central.

**Windows server 2012 R2 e Windows server 2012:** Esse parâmetro não está disponível antes do Windows Server 2016.

</dd> <dt>

*brokerDnsRRName* \[ no\]
</dt> <dd>

Nome DNS do agente.

</dd> <dt>

*activeBrokerName* \[ no\]
</dt> <dd>

Nome do agente ativo.

**Windows server 2012 R2 e Windows server 2012:** Esse parâmetro não está disponível antes do Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                         |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SessionBrokerServiceProperties Win32**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





