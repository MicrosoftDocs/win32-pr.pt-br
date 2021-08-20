---
title: Importando arquivos e bibliotecas de tipos
description: As palavras-chave MIDL incluem, Import e importlib permitem que você reutilize o código referenciando arquivos de cabeçalho, IDL e linguagem de definição de objeto (ODL) existentes e bibliotecas de tipos compiladas.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Linguagem IDL da Microsoft MIDL, tarefas, Importando arquivos e bibliotecas de tipos
- importando MIDL
- bibliotecas de tipos MIDL, importando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099ada5122ad024e342148bf3c453df0bd50872e6d59a2bbabd7d2892af5f93a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013734"
---
# <a name="importing-files-and-type-libraries"></a>Importando arquivos e bibliotecas de tipos

As palavras-chave MIDL [**incluem**](include.md), [**Import**](import.md)e [**importlib**](importlib.md) permitem que você reutilize o código referenciando arquivos de cabeçalho, IDL e linguagem de definição de objeto (ODL) existentes e bibliotecas de tipos compiladas.

A diretiva ACF [**include**](include.md) permite que você especifique em um arquivo ACF um ou mais arquivos de cabeçalho de linguagem C a serem incluídos no código stub gerado por MIDL. O arquivo gerado terá uma linha com uma diretiva **\# include** C-pré-processador com o arquivo de cabeçalho indicado. Use essa diretiva **include** para trazer arquivos de cabeçalho específicos para um determinado ambiente operacional e que não contêm informações necessárias para a interface entre o cliente e o servidor. Não use **include** para arquivos de cabeçalho que contenham tipos de dados que você deseja disponibilizar para o arquivo IDL; em vez disso, use a diretiva de [**importação**](import.md) .

## <a name="example-1"></a>Exemplo 1

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

A diretiva de [**importação**](import.md) de IDL é o método padrão para trazer definições de tipo e de interface de outros arquivos IDL (ou ODL) e arquivos de cabeçalho em seu arquivo IDL. Todas as instruções IDL no arquivo importado, como TYPEDEFs, declarações [**const**](const.md) e definições de interface, ficam disponíveis para o arquivo IDL de importação.

Assim como a diretiva de pré-processador de linguagem C **\# , a diretiva de** [**importação**](import.md) informa o compilador para incluir tipos de dados que foram definidos nos arquivos IDL importados. Ao contrário da diretiva **\# include** , a diretiva de **importação** ignora os protótipos de procedimento, pois nenhum stub é gerado para qualquer coisa no arquivo importado. Como o pré-processador é invocado separadamente para o arquivo importado, as diretivas de pré-processador (como * *) não são transportadas para o arquivo IDL de importação.

Para obter informações adicionais sobre como usar a [**importação**](import.md) para incluir arquivos de cabeçalho do sistema em um arquivo IDL, consulte [Importando arquivos de cabeçalho do sistema](importing-system-header-files.md).

## <a name="example-2"></a>Exemplo 2

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

A diretiva ODL [**importlib**](importlib.md) permite que você referencie uma biblioteca de tipos compilada em seu arquivo IDL ou ODL. A diretiva **importlib** deve estar dentro de uma instrução de [**biblioteca**](library.md) e deve preceder outras descrições de tipo na biblioteca. A biblioteca importada, bem como a biblioteca gerada, deve estar disponível para o aplicativo em tempo de execução.

## <a name="example-3"></a>Exemplo 3

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

Você também pode usar a diretiva C-pré-processador **\# include** para incluir cabeçalhos e outros arquivos em seu arquivo IDL ou ODL. No entanto, lembre-se de que essa diretiva incluirá literalmente todo o conteúdo do arquivo especificado. Se um arquivo de cabeçalho contiver protótipos que você não precisa ou deseja nos arquivos stub gerados por MIDL, ou se ele contiver definições de tipo não-Remotable, você deverá usar a diretiva de [**importação**](import.md) MIDL em vez da diretiva **\# include** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**importe**](import.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**incluir**](include.md)
</dt> <dt>

[Importar arquivos de cabeçalho do sistema](importing-system-header-files.md)
</dt> </dl>

 

 




