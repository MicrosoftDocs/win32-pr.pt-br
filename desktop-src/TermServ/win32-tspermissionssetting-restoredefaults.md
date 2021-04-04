---
title: Método RestoreDefaults da classe Win32_TSPermissionsSetting (Netfw. h)
description: Restaura os valores padrão do conjunto de permissões para o terminal.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RestoreDefaults
- Método RestoreDefaults Serviços de Área de Trabalho Remota, classe Win32_TSPermissionsSetting
- Classe Win32_TSPermissionsSetting Serviços de Área de Trabalho Remota, método RestoreDefaults
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824316"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a>Método RestoreDefaults da classe Win32 \_ TSPermissionsSetting

O método **RestoreDefaults** restaura os valores padrão do conjunto de permissões para o terminal.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna êxito em caso de êxito, caso contrário, falha.

## <a name="remarks"></a>Comentários

As permissões padrão são as seguintes:

-   As contas do assistente de ajuda de administradores, sistema e Área de Trabalho Remota têm todas as [permissões de serviços de área de trabalho remota](terminal-services-permissions.md).
-   A conta Área de Trabalho Remota usuários tem logon, conexão, informações de consulta e permissão para enviar mensagem.
-   O serviço local e as contas de serviço de rede têm informações de consulta e a permissão Enviar mensagem.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>Netfw. h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSPermissionsSetting Win32**](win32-tspermissionssetting.md)
</dt> </dl>

 

