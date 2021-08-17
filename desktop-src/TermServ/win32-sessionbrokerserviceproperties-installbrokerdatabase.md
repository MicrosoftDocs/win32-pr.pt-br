---
title: Método InstallBrokerDatabase da classe Win32_SessionBrokerServiceProperties
description: instala um banco de dados do agente de conexão RD em um servidor SQL central.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método InstallBrokerDatabase
- Método InstallBrokerDatabase Serviços de Área de Trabalho Remota, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Serviços de Área de Trabalho Remota, método InstallBrokerDatabase
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e77a34c70fbf06bac5501c8cacddce9feb9211d1fe21c1ef30fe429d3e75308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422446"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método InstallBrokerDatabase da classe Win32 \_ SessionBrokerServiceProperties

instala um banco de dados do agente de conexão RD em um servidor SQL central.

## <a name="syntax"></a>Sintaxe


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newDbFilePath* \[ no\]
</dt> <dd>

novo caminho do arquivo de banco de dados.

</dd> <dt>

*connStringToCentralDBMaster* \[ no\]
</dt> <dd>

Cadeia de conexão para o mestre do banco de dados central.

</dd> <dt>

*centralRdcmsDbName* \[ no\]
</dt> <dd>

Nome do banco de dados central.

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

 

 





