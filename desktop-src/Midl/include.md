---
title: atributo include
description: A instrução ACF include especifica um ou mais arquivos de header a serem incluídos no código stub gerado.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- atributo include MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ec8deec34a42d39fc3973dff73e9912ecb96bfee62e348ef7aebfee6ee9f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067197"
---
# <a name="include-attribute"></a>atributo include

A instrução **ACF include** especifica um ou mais arquivos de header a serem incluídos no código stub gerado.

``` syntax
include filenames;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nomes* 
</dt> <dd>

Especifica o nome de um ou mais arquivos de header da linguagem C. Use o nome completo do arquivo, incluindo o . Extensão H e coloque cada nome de arquivo entre aspas. Separe vários nomes de arquivo de header da linguagem C com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Como resultado da instrução **include,** o código stub gerado conterá uma instrução include do pré-processador **\# C.** Você fornece o arquivo de header da linguagem C ao compilar os stubs. As instruções Include dependem do mecanismo do compilador C para pesquisar arquivos incluídos na estrutura do diretório.

> [!Note]  
> Use a [**diretiva import**](import.md) em vez da **diretiva include** para arquivos do sistema que contêm tipos de dados que você deseja disponibilizar para o arquivo IDL. A **diretiva de** importação ignora os protótipos de função e permite que você use comutadores do compilador MIDL que otimizam a geração de rotinas de suporte.

 

## <a name="examples"></a>Exemplos

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Importação**](import.md)
</dt> <dt>

[Importando arquivos e bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> <dt>

[Importar arquivos de cabeçalho do sistema](importing-system-header-files.md)
</dt> </dl>

 

 




