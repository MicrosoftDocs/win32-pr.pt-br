---
title: Método SetEnforceChannelBinding da classe Win32_TSGatewayServerSettings dados
description: Define a propriedade EnforceChannelBinding.
ms.assetid: 8bd64fe7-bad5-44e6-a309-10802d9a8bd4
ms.tgt_platform: multiple
keywords:
- Método SetEnforceChannelBinding Serviços de Área de Trabalho Remota
- Método SetEnforceChannelBinding Serviços de Área de Trabalho Remota , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Serviços de Área de Trabalho Remota , método SetEnforceChannelBinding
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetEnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a2e076fb4ba439faa7cc22f30da1f815b0571ede0477b875e25176a7f0297e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988026"
---
# <a name="setenforcechannelbinding-method-of-the-win32_tsgatewayserversettings-class"></a>Método SetEnforceChannelBinding da classe \_ TSGatewayServerSettings do Win32

Define a **propriedade EnforceChannelBinding.**

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetEnforceChannelBinding(
  [in] boolean EnforceChannelBinding
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EnforceChannelBinding* \[ Em\]
</dt> <dd>

Especifica o novo valor da propriedade **EnforceChannelBinding.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                           |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





