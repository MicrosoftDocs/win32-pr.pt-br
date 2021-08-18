---
title: Método SetNetworkAdapterLanaID da classe Win32_TSNetworkAdapterSetting dados
description: Especifica o número DOL (Adaptador de Rede de Área Local) do adaptador de rede a ser definido.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- Método SetNetworkAdapterLanaID Serviços de Área de Trabalho Remota
- Método SetNetworkAdapterLanaID Serviços de Área de Trabalho Remota , Win32_TSNetworkAdapterSetting classe
- Win32_TSNetworkAdapterSetting classe Serviços de Área de Trabalho Remota , método SetNetworkAdapterLanaID
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5ffe976da794714f01e711913c01216d6b9bfad30c8c337da1fbd4c796e5f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008956"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a>Método SetNetworkAdapterLanaID da classe \_ TSNetworkAdapterSetting do Win32

O **método SetNetworkAdapterLanaID** especifica o número de ADAPTADOR DE REDE de Área Local do adaptador de rede a ser definido. Se a ID de LANG especificada não for válida ou não existir, um erro será retornado. A lista disponível de IDs DOIS é obtida enumerando a propriedade **DeviceIDList** na [**classe \_ Win32 TSNetworkAdapterSetting.**](win32-tsnetworkadaptersetting.md)

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NetworkAdapterLanaID* \[ Em\]
</dt> <dd>

Número DE VALOR do adaptador de rede a ser definido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

