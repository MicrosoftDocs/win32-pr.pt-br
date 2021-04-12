---
title: Classe Win32_TSGatewayServer
description: Usado para operações específicas de servidor do gateway de Área de Trabalho Remota (Gateway RD).
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayServer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayServer classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7dee009521c59b606010be085fcb0447558898d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455035"
---
# <a name="win32_tsgatewayserver-class"></a>\_Classe Win32 TSGatewayServer

Usado para operações específicas de servidor do gateway de Área de Trabalho Remota (Gateway RD).

## <a name="syntax"></a>Sintaxe

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSGatewayServer** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSGatewayServer** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**CreateSelfSignedCertificate**](createselfsignedcertificate-win32-tsgatewayserver.md) | Cria um certificado autoassinado com um determinado nome de entidade e retorna o hash de certificado como um parâmetro "out".<br/> |
| [**Exportação**](export-win32-tsgatewayserver.md)                                           | Retorna a configuração do servidor de gateway de área de trabalho remota como uma cadeia de caracteres XML.<br/>                                                       |
| [**Importar**](import-win32-tsgatewayserver.md)                                           | Importa uma determinada configuração para o servidor de gateway de área de trabalho remota.<br/>                                                             |



 

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



 

