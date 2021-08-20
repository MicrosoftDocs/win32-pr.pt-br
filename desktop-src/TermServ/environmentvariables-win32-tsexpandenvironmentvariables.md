---
title: Método EnvironmentVariables da classe Win32_TSExpandEnvironmentVariables
description: Expande variáveis de ambiente definidas pelo sistema. | Método EnvironmentVariables da classe Win32_TSExpandEnvironmentVariables
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnvironmentVariables
- Método EnvironmentVariables Serviços de Área de Trabalho Remota, classe Win32_TSExpandEnvironmentVariables
- Classe Win32_TSExpandEnvironmentVariables Serviços de Área de Trabalho Remota, método EnvironmentVariables
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49416291293d621739ab7c721ca349f5d87bb4582d1289f431a8c443d3414da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353888"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a>Método EnvironmentVariables da classe Win32 \_ TSExpandEnvironmentVariables

Expande variáveis de ambiente definidas pelo sistema.

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OriginalString* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que contém as variáveis de ambiente a serem expandidas.

</dd> <dt>

*Expandedstring* \[ fora\]
</dt> <dd>

Uma cadeia de caracteres com as variáveis de ambiente expandidas.

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

[**\_TSExpandEnvironmentVariables Win32**](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

