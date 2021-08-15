---
title: Método EnableRequestSOH da classe Win32_TSGatewayServerSettings dados
description: EnableRequestSOH não está mais disponível.
ms.assetid: 4feb7530-cced-4ead-a1fb-679b81442bb3
ms.tgt_platform: multiple
keywords:
- Método EnableRequestSOH Serviços de Área de Trabalho Remota
- Método EnableRequestSOH Serviços de Área de Trabalho Remota , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Serviços de Área de Trabalho Remota , método EnableRequestSOH
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableRequestSOH
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e1a3e4b6cf1312dde4dfc23105a32f6667667496a9a7162ad1b34cf34b2aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349150"
---
# <a name="enablerequestsoh-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnableRequestSOH da classe \_ Win32 TSGatewayServerSettings

\[O **método EnableRequestSOH** não está mais disponível desde Windows Server 2016.\]

Habilita ou desabilita solicitações para uma SoH (instrução de saúde).

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableRequestSOH(
  [in] boolean RequestSOH
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RequestSOH* \[ Em\]
</dt> <dd>

**Especifique TRUE** para habilitar o recurso **ou FALSE** para desabilitar o recurso.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Fim do suporte ao servidor<br/>    | Windows Server 2012 R2<br/>                                                        |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

