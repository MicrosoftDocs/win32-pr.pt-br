---
title: Método Export da classe Win32_TSVm
description: Recupera as informações de monitoramento da sessão de máquina virtual.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de exportação
- Método de exportação Serviços de Área de Trabalho Remota, classe Win32_TSVm
- Classe de Win32_TSVm Serviços de Área de Trabalho Remota, método de exportação
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764747"
---
# <a name="export-method-of-the-win32_tsvm-class"></a>Método Export da classe Win32 \_ TSVm

Recupera as informações de monitoramento da sessão de máquina virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ExportFolderPath* \[ no\]
</dt> <dd>

Caminho para onde a máquina virtual será exportada.

</dd> <dt>

*ExportJobObjectPath* \[ fora\]
</dt> <dd>

Em um êxito, retorna o caminho do objeto HyperV ConcreteJob.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSVm Win32**](win32-tsvm.md)
</dt> </dl>

 

 





