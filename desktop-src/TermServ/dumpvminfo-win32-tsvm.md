---
title: Método DumpVmInfo da classe Win32_TSVm
description: Esse membro é para fins de teste interno e não deve ser usado em seu código.
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DumpVmInfo
- Método DumpVmInfo Serviços de Área de Trabalho Remota, classe Win32_TSVm
- Classe Win32_TSVm Serviços de Área de Trabalho Remota, método DumpVmInfo
topic_type:
- apiref
api_name:
- Win32_TSVm.DumpVmInfo
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c74602e09f7aab4909e78bcd4696a450419e929b89769b35e16f21cbcafc080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354017"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a>Método DumpVmInfo da classe Win32 \_ TSVm

Esse membro é para fins de teste interno e não deve ser usado em seu código.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

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

 

 





