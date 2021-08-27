---
title: Método SelectNetworkAdapterIP da classe Win32_TSNetworkAdapterSetting
description: Seleciona um adaptador de rede com base no endereço IP do adaptador.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SelectNetworkAdapterIP
- Método SelectNetworkAdapterIP Serviços de Área de Trabalho Remota, classe Win32_TSNetworkAdapterSetting
- Classe Win32_TSNetworkAdapterSetting Serviços de Área de Trabalho Remota, método SelectNetworkAdapterIP
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a88c4820e4537d9c0fb1833b67eb2660a7fb5618189023dfe2217f222efa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008366"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a>Método SelectNetworkAdapterIP da classe Win32 \_ TSNetworkAdapterSetting

Seleciona um adaptador de rede com base no endereço IP do adaptador.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NetworkAdapterIP* \[ no\]
</dt> <dd>

O endereço IP do adaptador de rede a ser definido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero se o endereço IP especificado for válido e retornar um código de erro WMI se o endereço IP for inválido ou não existir. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="remarks"></a>Comentários

Você pode recuperar o endereço IP de um adaptador de rede enumerando as propriedades da classe [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) .

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSNetworkAdapterSetting Win32**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

