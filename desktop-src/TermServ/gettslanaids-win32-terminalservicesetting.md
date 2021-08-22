---
title: Método GetTSLanaIds da classe Win32_TerminalServiceSetting
description: Obtém as IDs do adaptador de rede de área local (LANA) do NetBIOS e as descrições de Serviços de Área de Trabalho Remota adaptadores de rede.
ms.assetid: 3f42e5da-c52b-4500-8cd0-52088dca544a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetTSLanaIds
- Método GetTSLanaIds Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método GetTSLanaIds
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTSLanaIds
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38c96c840879013f86339cd17136ea97a6c3da9933b1e409cf160779908e4038
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059574"
---
# <a name="gettslanaids-method-of-the-win32_terminalservicesetting-class"></a>Método GetTSLanaIds da classe Win32 \_ TerminalServiceSetting

O método **GetTSLanaIds** Obtém as IDs do adaptador de rede de área local (Lana) do NetBIOS e as descrições de serviços de área de trabalho remota adaptadores de rede.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetTSLanaIds(
  [out] uint32 LanaIdList[],
  [out] string LanaIdDescriptions[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LanaIdList* \[ fora\]
</dt> <dd>

Matriz de números de LANA.

</dd> <dt>

*LanaIdDescriptions* \[ fora\]
</dt> <dd>

Matriz de descrições de LANA correspondentes à matriz *LanaIdList* .

</dd> </dl>

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

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

