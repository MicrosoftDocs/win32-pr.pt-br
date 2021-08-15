---
title: Método SetPortNumbers da classe Win32_TSGatewayResourceAuthorizationPolicy dados
description: Define os números de porta que têm permissão para se conectar ao recurso por meio Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- Método SetPortNumbers Serviços de Área de Trabalho Remota
- Método SetPortNumbers Serviços de Área de Trabalho Remota , Win32_TSGatewayResourceAuthorizationPolicy classe
- Win32_TSGatewayResourceAuthorizationPolicy classe Serviços de Área de Trabalho Remota , método SetPortNumbers
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetPortNumbers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c151302abfda0b6bc42566770c0e8b8fb10dbab789cf2ece886be557efb023e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987766"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método SetPortNumbers da classe \_ Win32 TSGatewayResourceAuthorizationPolicy

Define os números de porta que têm permissão para se conectar ao recurso por meio Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PortNumbers* \[ Em\]
</dt> <dd>

Lista de números de porta separados por ponto e vírgula que são permitidos para este Área de Trabalho Remota política de autorização de recursos (RD FEDER). Para permitir qualquer número de porta, de definir " \* ".

</dd> </dl>

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

