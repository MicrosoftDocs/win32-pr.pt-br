---
title: atributo include
description: A instrução ACF include especifica um ou mais arquivos de cabeçalho a serem incluídos no código stub gerado.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- incluir o atributo MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084159"
---
# <a name="include-attribute"></a>atributo include

A instrução ACF **include** especifica um ou mais arquivos de cabeçalho a serem incluídos no código stub gerado.

``` syntax
include filenames;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nomes* 
</dt> <dd>

Especifica o nome de um ou mais arquivos de cabeçalho de linguagem C. Use o nome completo do arquivo, incluindo o. A extensão H e coloque cada nome de arquivo entre aspas. Separe vários nomes de arquivos de cabeçalho de linguagem C com vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Como resultado da instrução **include** , o código stub gerado conterá uma instrução C-pré-processador **\# include** . Você fornece o arquivo de cabeçalho de linguagem C ao compilar os stubs. As instruções include contam com o mecanismo do compilador C para pesquisar os arquivos incluídos na estrutura do diretório.

> [!Note]  
> Use a diretiva de [**importação**](import.md) em vez da diretiva **include** para arquivos do sistema que contêm tipos de dados que você deseja disponibilizar para o arquivo IDL. A diretiva de **importação** ignora protótipos de função e permite que você use opções de compilador MIDL que otimizam a geração de rotinas de suporte.

 

## <a name="examples"></a>Exemplos

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**importe**](import.md)
</dt> <dt>

[Importando arquivos e bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> <dt>

[Importar arquivos de cabeçalho do sistema](importing-system-header-files.md)
</dt> </dl>

 

 




