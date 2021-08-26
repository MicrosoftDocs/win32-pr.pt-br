---
title: /dlldata switch
description: A opção /dlldata é usada para especificar o nome do arquivo dlldata gerado para uma DLL proxy. O nome de arquivo padrão Dlldata.c será usado se a opção /dlldata não for especificada.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- /dlldata switch MIDL
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1274226ae9768d45bb11e1a1f5b55caeddcc247a74a7ac08e03e3fcdacb0e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105636"
---
# <a name="dlldata-switch"></a>/dlldata switch

A **opção /dlldata** é usada para especificar o nome do arquivo dlldata gerado para uma DLL proxy. O nome de arquivo padrão Dlldata.c será usado se a **opção /dlldata** não for especificada.

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*nome do arquivo* 
</dt> <dd>

O nome do arquivo de origem C que o compilador MIDL gerará para a DLL de proxy.

</dd> </dl>

## <a name="remarks"></a>Comentários

O arquivo especificado pelo *nome de arquivo* deve estar vinculado à DLL do proxy. O arquivo dlldata contém pontos de entrada e estruturas de dados exigidas pela fábrica de classes para a DLL proxy. Essas estruturas de dados especificam as interfaces de objeto contidas na DLL de proxy. O arquivo dlldata também especifica o identificador de classe da fábrica de classes para a DLL proxy. Esse é sempre o IID (UUID) da primeira interface do primeiro arquivo proxy (por ordem alfabética).

O mesmo arquivo dlldata deve ser especificado ao invocar MIDL em todos os arquivos IDL que entrarão em uma DLL de proxy específica. O arquivo dlldata é criado ou atualizado durante cada compilação MIDL, criando incrementalmente uma lista das interfaces que entrarão na DLL do proxy.

## <a name="examples"></a>Exemplos

**midl /dlldata data.c**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




