---
title: Método InitialProgram da classe Win32_TSEnvironmentSetting
description: O método InitialProgram define as propriedades do programa de inicialização, como o nome, o diretório de trabalho e o caminho do programa para iniciar imediatamente após o logon no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método InitialProgram
- Método InitialProgram Serviços de Área de Trabalho Remota, classe Win32_TSEnvironmentSetting
- Classe Win32_TSEnvironmentSetting Serviços de Área de Trabalho Remota, método InitialProgram
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd41e1af990e37b8458431106bc2ec9a8489b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760120"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a>Método InitialProgram da classe Win32 \_ TSEnvironmentSetting

O método **InitialProgram** define as propriedades do programa de inicialização, como o nome, o diretório de trabalho e o caminho do programa para iniciar imediatamente após o logon no servidor de Host da Sessão da Área de Trabalho Remota (host da Sessão RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*InitialProgramPath* \[ no\]
</dt> <dd>

O nome e o caminho do programa de inicialização.

</dd> <dt>

*Início* \[ no\]
</dt> <dd>

O caminho para o diretório de trabalho do programa de inicialização.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_TSEnvironmentSetting Win32**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

