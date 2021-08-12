---
title: Método FileExtensions da classe Win32_TSApplicationFileExtensions
description: Fornece uma lista das extensões de nome de arquivo que são manipuladas por um aplicativo.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- Método de extensões de fileServiços de Área de Trabalho Remota
- Método de extensões de fileServiços de Área de Trabalho Remota, classe Win32_TSApplicationFileExtensions
- Classe de Win32_TSApplicationFileExtensions Serviços de Área de Trabalho Remota, método FileExtensions
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c7c44acd410566c4f048cdf36bac904c18b21df42f53543051e3b94f49bfbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609368"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a>Método FileExtensions da classe Win32 \_ TSApplicationFileExtensions

Fornece uma lista das extensões de nome de arquivo que são manipuladas por um aplicativo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AppPath* \[ no\]
</dt> <dd>

O caminho do aplicativo.

</dd> <dt>

*Extensões* \[ do fora\]
</dt> <dd>

As extensões de nome de arquivo que são manipuladas pelo aplicativo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSApplicationFileExtensions Win32**](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

