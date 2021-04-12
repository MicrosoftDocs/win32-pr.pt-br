---
title: Método IsDbReachable da classe Win32_SessionBrokerServiceProperties
description: Verifica se o banco de dados está acessível.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsDbReachable
- Método IsDbReachable Serviços de Área de Trabalho Remota, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Serviços de Área de Trabalho Remota, método IsDbReachable
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a59b8b0eba80dd832b3967b5e626642684f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455137"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método IsDbReachable da classe Win32 \_ SessionBrokerServiceProperties

Verifica se o banco de dados está acessível.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*connStringToDb* \[ no\]
</dt> <dd>

A cadeia de conexão para o banco de dados.

</dd> <dt>

*connSecondaryStringToDb* \[ no\]
</dt> <dd>

Cadeia de conexão secundária para o banco de dados central.

**Windows server 2012 R2 e Windows server 2012:** Esse parâmetro não está disponível antes do Windows Server 2016.

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

 

 





