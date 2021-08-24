---
title: Método SelectNetworkAdapter da Win32_TSVirtualIP classe
description: Define o endereço MAC do adaptador de rede a ser usado para virtualização de IP.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- Método SelectNetworkAdapter Serviços de Área de Trabalho Remota
- Método SelectNetworkAdapter Serviços de Área de Trabalho Remota , Win32_TSVirtualIP classe
- Win32_TSVirtualIP classe Serviços de Área de Trabalho Remota , método SelectNetworkAdapter
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d27df38f8314720c4ed16d675cdbd06424611d2ccd127a45069586875c82d77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865516"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a>Método SelectNetworkAdapter da classe \_ Win32 TSVirtualIP

Define o endereço MAC do adaptador de rede a ser usado para virtualização de IP.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NetworkAdapterMacAddress* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Especifica o endereço MAC do adaptador de rede.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

Se o endereço MAC for inválido ou não existir ou se o modo de virtualização de IP for por sessão, um erro será retornado.

O método retornará um erro se a configuração estiver sob controle de política de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





