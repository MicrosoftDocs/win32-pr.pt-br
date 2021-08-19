---
title: Método RemoveProgram da classe Win32_TSVirtualIP (Bdaiface. h)
description: Remove um programa da lista de programas que usam a virtualização de IP.
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveProgram
- Método RemoveProgram Serviços de Área de Trabalho Remota, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Serviços de Área de Trabalho Remota, método RemoveProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44d955c7547a308086ea365681a5991012fe65e390ebe296f031f0c0ef99856
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058614"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a>Método RemoveProgram da classe Win32 \_ TSVirtualIP

Remove um programa da lista de programas que usam a virtualização de IP.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProgramPath* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

O caminho e o nome do arquivo do programa a ser removido da lista. Se o programa não for encontrado, um erro será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>Bdaiface. h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





