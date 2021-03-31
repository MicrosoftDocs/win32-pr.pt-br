---
title: Usando MIDL
description: Criar e compilar uma interface linguagem IDL da Microsoft (MIDL) e uma chamada de procedimento remoto (RPC).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da60f20cba6c558c7f1a67478adef7b407d591
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641778"
---
# <a name="using-midl"></a>Usando MIDL

Todas as interfaces para programas que usam RPC devem ser definidas em linguagem IDL da Microsoft (MIDL) e compiladas com o compilador MIDL. Os tópicos a seguir apresentam uma breve visão geral da criação e da compilação de uma interface MIDL:

-   [Definindo uma interface com MIDL](#defining-an-interface-with-midl)
-   [Compilando um arquivo MIDL](#compiling-a-midl-file)

Para obter uma discussão detalhada sobre esses tópicos, consulte [os arquivos IDL e ACF](the-idl-and-acf-files.md).

## <a name="defining-an-interface-with-midl"></a>Definindo uma interface com MIDL

Os arquivos MIDL são arquivos de texto que você pode criar e editar com um editor de texto. Se você gerar um UUID para sua interface, você normalmente armazenará a saída em um arquivo MIDL de modelo. Para obter mais informações sobre UUIDs, consulte [gerando UUIDs de interface](generating-interface-uuids.md).

Todas as interfaces no MIDL seguem o mesmo formato. Eles começam com um cabeçalho que contém uma lista de atributos de interface e o nome da interface. Os atributos são colocados entre colchetes. O cabeçalho da interface é seguido por seu corpo, que é colocado entre chaves. Uma interface simples é mostrada no exemplo a seguir:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface MyInterface
{
  const unsigned short INT_ARRAY_LEN = 100;

  void MyRemoteProc( 
      [in] int param1,
      [out] int outArray[INT_ARRAY_LEN]
  );
}
```

Alguns dos atributos que normalmente aparecem em uma definição de interface MIDL são o UUID e o número de versão da interface. O corpo da definição de interface deve conter as declarações de procedimento de todos os procedimentos remotos na interface. Ele também pode conter as declarações de tipos de dados e constantes exigidas pela interface.

Todos os parâmetros nas declarações de procedimento remoto devem ser declarados como \[ [**in**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl) \] ou \[ **in**, **out** \] . Essas declarações especificam que o programa cliente passa dados para um procedimento remoto, obtém dados de um procedimento remoto ou ambos. Para obter informações mais detalhadas sobre declarações de parâmetro de interface, consulte [o corpo da interface IDL](the-idl-interface-body.md).

## <a name="compiling-a-midl-file"></a>Compilando um arquivo MIDL

O compilador MIDL é uma ferramenta de linha de comando que é instalada automaticamente com o SDK (Software Development Kit) da plataforma. Invoque-o em uma janela de comando digitando o comando **MIDL**, seguido pelo nome de um arquivo MIDL, na linha de comando. Verifique se o diretório que contém o compilador MIDL está em seu caminho. O exemplo a seguir ilustra seu uso:

**MIDL MyApp. idl**

Observe que você não precisa incluir a extensão se o nome do arquivo tiver a extensão. idl. Você também pode usar as opções de [linha de comando](/windows/desktop/Midl/midl-command-line-reference) do compilador MIDL inserindo-as entre o comando **MIDL** e o nome do arquivo. Isso é demonstrado no exemplo a seguir:

**MIDL/ACF MyApp. ACF MyApp. idl**

Neste exemplo, o compilador MIDL é executado usando o arquivo MyApp. idl como o arquivo de entrada. A opção de linha de comando **/ACF** instrui o compilador a usar um ACF (arquivo de configuração de aplicativo) para entrada também. Os arquivos de configuração de aplicativo são discutidos mais detalhadamente nos [arquivos IDL e ACF](the-idl-and-acf-files.md).

Para obter informações mais detalhadas sobre como usar o compilador MIDL, consulte o [linguagem IDL da Microsoft (MIDL)](/windows/desktop/Midl/midl-start-page), que contém informações sobre os seguintes tópicos:

-   [Requisitos de pré-processador do C para MIDL](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [C/C++-considerações do compilador](/windows/desktop/Midl/c-c-compiler-considerations)
-   [Arquivos gerados para uma interface RPC](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [Referência de linha de comando MIDL](/windows/desktop/Midl/midl-command-line-reference)
-   [Referência da linguagem MIDL](/windows/desktop/Midl/midl-language-reference)
-   [Erros e avisos do compilador MIDL](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 