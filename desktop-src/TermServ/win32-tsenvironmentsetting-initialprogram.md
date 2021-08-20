---
title: Método InitialProgram da classe Win32_TSEnvironmentSetting dados
description: O método InitialProgram define as propriedades do programa de inicialização, como o nome, o diretório de trabalho e o caminho do programa a iniciar imediatamente após o logon no servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- Método InitialProgram Serviços de Área de Trabalho Remota
- Método InitialProgram Serviços de Área de Trabalho Remota , Win32_TSEnvironmentSetting classe
- Win32_TSEnvironmentSetting classe Serviços de Área de Trabalho Remota , método InitialProgram
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
ms.openlocfilehash: 9d13aaa0e4dfb4e0d16bea89bf871a7a890c0f375fd928e70fd99aed20c003be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126982"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a>Método InitialProgram da classe \_ Win32 TSEnvironmentSetting

O **método InitialProgram** define as propriedades do programa de inicialização, como o nome, o diretório de trabalho e o caminho do programa para iniciar imediatamente após o logon no servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*InitialProgramPath* \[ Em\]
</dt> <dd>

O nome e o caminho do programa de inicialização.

</dd> <dt>

*Startin* \[ Em\]
</dt> <dd>

O caminho para o diretório de trabalho do programa de inicialização.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de política de grupo.

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

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

