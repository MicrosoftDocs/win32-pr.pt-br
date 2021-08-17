---
title: Método AddProgram da classe Win32_TSVirtualIP (Bdaiface.h)
description: Adiciona um programa à lista de programas que usam a virtualização de IP.
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- Método AddProgram Serviços de Área de Trabalho Remota
- Método AddProgram Serviços de Área de Trabalho Remota , Win32_TSVirtualIP classe
- Win32_TSVirtualIP classe Serviços de Área de Trabalho Remota , método AddProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2f78cb461a61467867a544e954a71c23d59432e29450a7b0f35184f0edec57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757851"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a>Método AddProgram da classe \_ Win32 TSVirtualIP

Adiciona um programa à lista de programas que usam a virtualização de IP.

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProgramPath* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

O caminho e o nome do arquivo do programa a adicionar à lista.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de política de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>Bdaiface.h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





