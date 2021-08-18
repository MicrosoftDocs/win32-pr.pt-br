---
title: Método GetIcon da classe Win32_TSGetIcon
description: Retorna o conteúdo do ícone especificado.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- Método GetIcon Serviços de Área de Trabalho Remota
- Método GetIcon Serviços de Área de Trabalho Remota, classe Win32_TSGetIcon
- Classe Win32_TSGetIcon Serviços de Área de Trabalho Remota, método GetIcon
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305316d66ce95659210396a10f22366d64ebdd2b410b056aa3c398cf65edbbf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001534"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a>Método GetIcon da \_ classe TSGetIcon do Win32

Retorna o conteúdo do ícone especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FilePath* \[ no\]
</dt> <dd>

Especifica o caminho para o arquivo que contém o ícone

</dd> <dt>

*Índice* \[ do no\]
</dt> <dd>

Especifica o índice do ícone no arquivo.

</dd> <dt>

*IconContents* \[ fora\]
</dt> <dd>

Em conclusão bem-sucedida, contém o conteúdo do ícone.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGetIcon Win32**](win32-tsgeticon.md)
</dt> </dl>

 

 





