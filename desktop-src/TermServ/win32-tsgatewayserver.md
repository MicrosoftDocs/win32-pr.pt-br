---
title: Win32_TSGatewayServer classe
description: Usado para operações específicas de servidor Área de Trabalho Remota Gateway de Área de Trabalho Área de Trabalho Remota (Gateway de Área de Trabalho Local).
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServer classe Serviços de Área de Trabalho Remota
- Win32_TSGatewayServer classe Serviços de Área de Trabalho Remota , descrito
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
ms.openlocfilehash: 43cd6c24447e7ba3bc22788484b2ac9e437ee947243c17a676728d2a336bd326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603877"
---
# <a name="win32_tsgatewayserver-class"></a>Classe Win32 \_ TSGatewayServer

Usado para operações específicas de servidor Área de Trabalho Remota Gateway de Área de Trabalho Área de Trabalho Remota (Gateway de Área de Trabalho Local).

## <a name="syntax"></a>Sintaxe

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a>Membros

A **classe \_ Win32 TSGatewayServer** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **classe \_ Win32 TSGatewayServer** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**CreateSelfSignedCertificate**](createselfsignedcertificate-win32-tsgatewayserver.md) | Cria um certificado auto-assinado com um determinado nome de assunto e retorna o hash do certificado como um parâmetro "out".<br/> |
| [**Exportação**](export-win32-tsgatewayserver.md)                                           | Retorna a configuração do servidor do Gateway de Área de Trabalho Avançada como uma cadeia de caracteres XML.<br/>                                                       |
| [**Importar**](import-win32-tsgatewayserver.md)                                           | Importa uma determinada configuração para o servidor de Gateway de RD.<br/>                                                             |



 

## <a name="remarks"></a>Comentários

Managed Object Format arquivos (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



 

