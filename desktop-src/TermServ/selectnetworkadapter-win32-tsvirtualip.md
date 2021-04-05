---
title: Método SelectNetworkAdapter da classe Win32_TSVirtualIP
description: Define o endereço MAC do adaptador de rede a ser usado para virtualização de IP.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SelectNetworkAdapter
- Método SelectNetworkAdapter Serviços de Área de Trabalho Remota, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Serviços de Área de Trabalho Remota, método SelectNetworkAdapter
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
ms.openlocfilehash: a3a362bea1a5cacbfd727f23504f19164c79ce65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918367"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a>Método SelectNetworkAdapter da classe Win32 \_ TSVirtualIP

Define o endereço MAC do adaptador de rede a ser usado para virtualização de IP.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NetworkAdapterMacAddress* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Especifica o endereço MAC do adaptador de rede.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

Se o endereço MAC for inválido ou não existir, ou se o modo de virtualização de IP for por sessão, um erro será retornado.

O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





