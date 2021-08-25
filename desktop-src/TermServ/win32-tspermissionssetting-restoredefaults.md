---
title: Método RestoreDefaults da classe Win32_TSPermissionsSetting (Netfw.h)
description: Restaura os valores de conjunto de permissões padrão para o terminal.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Método RestoreDefaults Serviços de Área de Trabalho Remota
- Método RestoreDefaults Serviços de Área de Trabalho Remota classe Win32_TSPermissionsSetting ,
- Win32_TSPermissionsSetting classe Serviços de Área de Trabalho Remota , método RestoreDefaults
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
ms.openlocfilehash: 8ef81f4b3008f68129026a90d1b2e98e8c13c298537952175e116c9c8e02c4f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769446"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a>Método RestoreDefaults da classe \_ Win32 TSPermissionsSetting

O **método RestoreDefaults** restaura os valores de conjunto de permissões padrão para o terminal.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna Êxito em caso de êxito, caso contrário, Falha.

## <a name="remarks"></a>Comentários

As permissões padrão são as seguintes:

-   As contas administradores, sistema e Área de Trabalho Remota assistente de ajuda têm [todas as Serviços de Área de Trabalho Remota permissões](terminal-services-permissions.md).
-   A Área de Trabalho Remota Usuários tem a permissão Logon, Conexão, Informações de Consulta e Enviar Mensagem.
-   As contas serviço local e serviço de rede têm informações de consulta e permissão Enviar Mensagem.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>Netfw.h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

