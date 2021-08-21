---
title: Método SetBrokerHAMode da classe Win32_SessionBrokerServiceProperties classe
description: Migra dados de um banco de dados WID local para o novo banco SQL banco de dados baseado em servidor. Ele também configura o servidor agente para usar o servidor SQL central.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Método SetBrokerHAMode Serviços de Área de Trabalho Remota
- Método SetBrokerHAMode Serviços de Área de Trabalho Remota , Win32_SessionBrokerServiceProperties classe
- Win32_SessionBrokerServiceProperties classe Serviços de Área de Trabalho Remota , método SetBrokerHAMode
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
ms.openlocfilehash: 17b72233b51686911e4b1d0a661f4e46fa9bcaa813bb6ccc973b2f8a5b12da24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604545"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método SetBrokerHAMode da classe \_ SessionBrokerServiceProperties do Win32

Migra dados de um banco de dados WID local para o novo banco SQL banco de dados baseado em servidor. Ele também configura o servidor agente para usar o servidor SQL central.

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

*connStringToCentralDBRdcms* \[ Em\]
</dt> <dd>

Cadeia de conexão com o banco de dados central.

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[ Em\]
</dt> <dd>

Cadeia de conexão secundária para o banco de dados central.

**Windows Server 2012 R2 e Windows Server 2012:** Esse parâmetro não está disponível antes Windows Server 2016.

</dd> <dt>

*brokerDnsRRName* \[ Em\]
</dt> <dd>

Nome DNS do agente.

</dd> <dt>

*activeBrokerName* \[ Em\]
</dt> <dd>

Nome do agente ativo.

**Windows Server 2012 R2 e Windows Server 2012:** Esse parâmetro não está disponível antes Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                         |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





