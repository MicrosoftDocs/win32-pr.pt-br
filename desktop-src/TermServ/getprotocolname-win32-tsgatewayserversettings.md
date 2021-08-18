---
title: Método GetProtocolName da classe Win32_TSGatewayServerSettings classe
description: Retorna o nome do protocolo para o índice de protocolo especificado.
ms.assetid: 6778cede-cc61-4e5d-9a29-ba88197fa8c6
ms.tgt_platform: multiple
keywords:
- Método GetProtocolName Serviços de Área de Trabalho Remota
- Método GetProtocolName Serviços de Área de Trabalho Remota , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Serviços de Área de Trabalho Remota , método GetProtocolName
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetProtocolName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b70ee57d8940dc65b1f7b74151a3dd6889286a26e7bbf4357bea4aae8c5259
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757818"
---
# <a name="getprotocolname-method-of-the-win32_tsgatewayserversettings-class"></a>Método GetProtocolName da classe \_ Win32 TSGatewayServerSettings

Retorna o nome do protocolo para o índice de protocolo especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetProtocolName(
  [in]  uint32 ProtocolId,
  [out] string ProtocolName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtocolId* \[ Em\]
</dt> <dd>

Índice do identificador de protocolo. O valor deve estar entre zero e o valor da **propriedade MaxProtocols.**

</dd> <dt>

*ProtocolName* \[ out\]
</dt> <dd>

Retorna o nome do protocolo especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Há suporte para um protocolo.

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

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

