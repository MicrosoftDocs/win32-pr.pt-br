---
title: Método Delete da classe Win32_Terminal
description: Exclui o terminal especificado.
ms.assetid: 59d8cc73-aef1-49d2-a7a2-dd3cbe5a8c52
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método Delete
- Método Delete Serviços de Área de Trabalho Remota, classe Win32_Terminal
- Classe Win32_Terminal Serviços de Área de Trabalho Remota, método Delete
topic_type:
- apiref
api_name:
- Win32_Terminal.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5e1e91077cfbabb1e00db29b186db5b19f6333be77cf27ec2307cc8ffeff18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609648"
---
# <a name="delete-method-of-the-win32_terminal-class"></a>Método Delete da \_ classe terminal do Win32

O método **delete** exclui o terminal especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Delete(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NewTerminalName* \[ no\]
</dt> <dd>

Nome do terminal a ser excluído.

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

[**Terminal do Win32 \_**](win32-terminal.md)
</dt> </dl>

 

