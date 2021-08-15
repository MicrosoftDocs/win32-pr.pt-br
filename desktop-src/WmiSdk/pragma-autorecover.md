---
description: Adiciona um arquivo MOF à lista de arquivos compilados durante a recuperação do repositório.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma AutoRecuperação
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: cc36191482731e77d0f82c4e3734350da2f6ed2fbd3faad7b2972dca4e0e6bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992696"
---
# <a name="pragma-autorecover"></a>pragma AutoRecuperação

O comando **pragma autocover** pré-processador adiciona um arquivo MOF à lista de arquivos compilados durante a recuperação do repositório. A lista de arquivos MOF de **recuperação automática** está armazenada nesta chave do registro:

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AutoRecuperação MOFs**

O WMI verifica a integridade do repositório do WMI quando o sistema operacional inicia o WMI. Se o repositório estiver danificado, o WMI recompilará automaticamente o repositório e recompilará todos os arquivos MOF listados nessa chave no registro.

O seguinte descreve a sintaxe para o comando pragma Recover:


```mof
#pragma autorecover
```



No entanto, você deve observar as seguintes restrições ao usar este comando:

-   O WMI não pode recuperar arquivos MOF localizados em um computador remoto.

    Portanto, os arquivos MOF listados nesta chave do registro devem residir no computador local.

-   Você não pode especificar as opções de linha de comando que o compilador MOF usa quando o WMI recupera um arquivo MOF.

    Portanto, você deve incluir comandos [pragma](-pragma.md) no arquivo MOF que tornam as opções de linha de comando desnecessárias. O exemplo a seguir descreve uma opção de linha de comando comum que o WMI não usa ao recuperar um arquivo MOF desta chave do registro: **Mofcomp-N:root \\ Test mymof. mof**

    No entanto, você pode especificar o namespace usando um comando [pragma](-pragma.md) no arquivo MOF.

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
    ```

    

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Comandos de pré-processador](preprocessor-commands.md)
</dt> </dl>

 

 




