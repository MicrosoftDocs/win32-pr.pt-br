---
title: Método SelectAllNetworkAdapters da classe Win32_TSNetworkAdapterSetting
description: O método SelectAllNetworkAdapters seleciona todos os adaptadores de rede.
ms.assetid: e0bd60c3-55c3-4be9-be2d-3b97db3047d9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SelectAllNetworkAdapters
- Método SelectAllNetworkAdapters Serviços de Área de Trabalho Remota, classe Win32_TSNetworkAdapterSetting
- Classe Win32_TSNetworkAdapterSetting Serviços de Área de Trabalho Remota, método SelectAllNetworkAdapters
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectAllNetworkAdapters
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a359e3ea87c1c2f4567e752a714741c0f2617304f8d261e0baf811794d788895
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119420516"
---
# <a name="selectallnetworkadapters-method-of-the-win32_tsnetworkadaptersetting-class"></a>Método SelectAllNetworkAdapters da classe Win32 \_ TSNetworkAdapterSetting

O método **SelectAllNetworkAdapters** seleciona todos os adaptadores de rede.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SelectAllNetworkAdapters();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="remarks"></a>Comentários

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

 

