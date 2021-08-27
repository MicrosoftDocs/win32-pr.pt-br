---
title: Usando MIDL
description: Criando e compilando uma interface LINGUAGEM IDL DA MICROSOFT (MIDL) e uma RPC (Chamada de Procedimento Remoto).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ae89a740831fef28ade4c07dc6bbe2b9b68a8a154eb119f47e16b2cb68b325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010744"
---
# <a name="using-midl"></a>Usando MIDL

Todas as interfaces para programas que usam RPC devem ser definidas em linguagem IDL da Microsoft (MIDL) e compiladas com o compilador MIDL. Os tópicos a seguir apresentam uma breve visão geral da criação e compilação de uma interface MIDL:

-   [Definindo uma interface com MIDL](#defining-an-interface-with-midl)
-   [Compilando um arquivo MIDL](#compiling-a-midl-file)

Para uma discussão detalhada sobre esses tópicos, consulte [Os arquivos IDL e ACF](the-idl-and-acf-files.md).

## <a name="defining-an-interface-with-midl"></a>Definindo uma interface com MIDL

Arquivos MIDL são arquivos de texto que você pode criar e editar com um editor de texto. Se você gerar um UUID para sua interface, normalmente armazenará a saída em um arquivo MIDL de modelo. Para obter mais informações sobre UUIDs, consulte [Gerando UUIDs de interface](generating-interface-uuids.md).

Todas as interfaces em MIDL seguem o mesmo formato. Eles começam com um header que contém uma lista de atributos de interface e o nome da interface. Os atributos são incluídos entre colchetes. O título da interface é seguido por seu corpo, que é entre colchetes. Uma interface simples é mostrada no exemplo a seguir:

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

Alguns dos atributos que normalmente aparecem em uma definição de interface MIDL são o UUID e o número de versão da interface. O corpo da definição da interface deve conter as declarações de procedimento de todos os procedimentos remotos na interface. Ele também pode conter as declarações de tipos de dados e constantes exigidas pela interface .

Todos os parâmetros nas declarações de procedimento remoto devem ser declarados como \[ [**em**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl) \] ou \[ **em**, **out** \] . Essas declarações especificam que o programa cliente passa dados para um procedimento remoto, obtém dados de um procedimento remoto ou ambos. Para obter informações mais detalhadas sobre declarações de parâmetro de interface, consulte [O corpo da interface IDL](the-idl-interface-body.md).

## <a name="compiling-a-midl-file"></a>Compilando um arquivo MIDL

O compilador MIDL é uma ferramenta de linha de comando instalada automaticamente com o SDK (Kit de Desenvolvimento de Software de Plataforma). Invoque-o em uma janela de comando digitando o comando **midl**, seguido pelo nome de um arquivo MIDL, na linha de comando. Certifique-se de que o diretório que contém o compilador MIDL está em seu caminho. O exemplo a seguir ilustra seu uso:

**midl MyApp.idl**

Observe que você não precisa incluir a extensão se o nome do arquivo tiver a extensão .idl. Você também pode usar as opções de linha de comando do compilador MIDL [inserindo-as](/windows/desktop/Midl/midl-command-line-reference) entre o comando **midl** e o nome do arquivo. Isso é demonstrado no exemplo a seguir:

**midl /acf MyApp.acf MyApp.idl**

Neste exemplo, o compilador MIDL é executado usando o arquivo MyApp.idl como o arquivo de entrada. A opção de linha de comando **/acf** instrui o compilador a usar um arquivo de configuração de aplicativo (ACF) para entrada também. Os arquivos de configuração de aplicativo são discutidos mais detalhadamente [em Arquivos IDL e ACF.](the-idl-and-acf-files.md)

Para obter informações mais detalhadas sobre como usar o compilador MIDL, consulte o [linguagem IDL da Microsoft (MIDL),](/windows/desktop/Midl/midl-start-page)que contém informações sobre os tópicos a seguir:

-   [Requisitos do pré-processador C para MIDL](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [Considerações do compilador C/C++](/windows/desktop/Midl/c-c-compiler-considerations)
-   [Arquivos gerados para uma interface RPC](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [Referência de linha de comando MIDL](/windows/desktop/Midl/midl-command-line-reference)
-   [Referência da linguagem MIDL](/windows/desktop/Midl/midl-language-reference)
-   [Erros e avisos do compilador MIDL](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 