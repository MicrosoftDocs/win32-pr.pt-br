---
title: comutador/dlldata nomedearquivo
description: A opção/dlldata nomedearquivo é usada para especificar o nome do arquivo dlldata gerado para uma DLL de proxy. O nome de arquivo padrão dlldata. c será usado se a opção/dlldata nomedearquivo não for especificada.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- MIDL do comutador/dlldata nomedearquivo
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e9c1d7f27c56f81905081fd9ef24c8c490391b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638632"
---
# <a name="dlldata-switch"></a>comutador/dlldata nomedearquivo

A opção **/dlldata nomedearquivo** é usada para especificar o nome do arquivo dlldata gerado para uma DLL de proxy. O nome de arquivo padrão dlldata. c será usado se a opção **/dlldata nomedearquivo** não for especificada.

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*nome do arquivo* 
</dt> <dd>

O nome do arquivo de origem C que o compilador MIDL irá gerar para a DLL de proxy.

</dd> </dl>

## <a name="remarks"></a>Comentários

O arquivo especificado por *nome de arquivo* deve ser vinculado à dll de proxy. O arquivo dlldata contém pontos de entrada e estruturas de dados exigidos pela fábrica de classes para a DLL de proxy. Essas estruturas de dados especificam as interfaces de objeto contidas na DLL de proxy. O arquivo dlldata também especifica o identificador de classe da fábrica de classes para a DLL de proxy. Esse é sempre o UUID (IID) da primeira interface do primeiro arquivo de proxy (por ordem alfabética).

O mesmo arquivo dlldata deve ser especificado ao invocar MIDL em todos os arquivos IDL que entrarão em uma DLL de proxy específica. O arquivo dlldata é criado ou atualizado durante cada compilação de MIDL, criando incrementalmente uma lista das interfaces que entrarão na DLL de proxy.

## <a name="examples"></a>Exemplos

**MIDL/dlldata nomedearquivo Data. c**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




