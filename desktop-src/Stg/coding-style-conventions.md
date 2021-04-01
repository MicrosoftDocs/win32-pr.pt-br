---
title: Convenções de estilo de codificação
description: As convenções de estilo de codificação são usadas nesta série de exemplo para auxiliar na clareza e na consistência.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103643015"
---
# <a name="coding-style-conventions"></a>Convenções de estilo de codificação

As convenções de estilo de codificação são usadas nesta série de exemplo para auxiliar na clareza e na consistência. As convenções de notação "húngaro" são usadas. Elas se tornaram uma prática de codificação comum na programação do Win32. Eles incluem notações de prefixo variável que fornecem a nomes de variáveis uma sugestão do tipo da variável.

A tabela a seguir lista os prefixos comuns.



| Prefixo | Descrição                         |
|--------|-------------------------------------|
| um      | Array                               |
| b      | BOOL (int)                          |
| c      | Char                                |
| CB     | Contagem de bytes                      |
| CD     | Valor de referência de cor               |
| CX     | Contagem de x (curta)                  |
| dw     | DWORD (longo sem sinal)               |
| f      | Flags (geralmente valores de vários bits) |
| fn     | Função                            |
| m\_    | Global                              |
| h      | Handle                              |
| i      | Integer                             |
| l      | long                                |
| lp     | Ponteiro longo                        |
| d\_    | Membro de dados de uma classe              |
| n      | Int curta                           |
| p      | Ponteiro                             |
| s      | String                              |
| sz     | Cadeia de caracteres terminada em zero              |
| tm     | Métrica de texto                         |
| u      | Int não assinado                        |
| UL     | Longo não atribuído (ULONG)               |
| w      | PALAVRA (sem sinal curto)               |
| x, y    | coordenadas x, y (abreviadas)            |



 

Essas muitas vezes são combinadas, como no seguinte.



| Combinação de prefixo | Descrição                                             |
|--------------------|---------------------------------------------------------|
| pszMyString        | Um ponteiro para uma cadeia de caracteres.                                  |
| \_pszMyString m     | Um ponteiro para uma cadeia de caracteres que é um membro de dados de uma classe. |



 

Outras convenções são listadas na tabela a seguir.



| Convenção       | Descrição                                              |
|------------------|----------------------------------------------------------|
| CMyClass         | Prefixo ' C' para nomes de classe C++.                          |
| COMyObjectClass  | Prefixo ' CO ' para nomes de classe de objeto COM.                  |
| CFMyClassFactory | Prefixo ' CF ' para nomes de fábrica de classes COM.                 |
| IMinhaInterface     | Prefixo ' I ' para nomes de classe de interface COM.                |
| CImpIMyInterface | Prefixo ' CImpI ' para classes de implementação de interface COM. |



 

Algumas convenções consistentes para blocos de cabeçalho de comentário são usadas nesta série de exemplo da seguinte maneira.

## <a name="file-header"></a>Cabeçalho do arquivo

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a>Bloco de comentário simples

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a>Cabeçalho de declaração de classe

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a>Cabeçalho de definição do método de classe

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a>Função local ou não exportada

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a>Cabeçalho de definição de função exportada

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a>Cabeçalho de declaração da interface COM

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a>Cabeçalho de declaração de classe de objeto COM

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

Todas essas convenções de bloco de comentário têm cadeias de caracteres de token de início e término consistentes. Essa consistência dá suporte ao processamento automático dos cabeçalhos de alguma maneira. Por exemplo, os scripts AWK podem ser gravados para filtrar os cabeçalhos de função em um arquivo de texto separado que pode servir como base para um documento de especificação. Da mesma forma, ferramentas como o utilitário autopato sem suporte (atualmente disponível no CD-ROM da biblioteca de desenvolvimento do Microsoft Developer Network) podem ser usadas para processar os blocos de comentário nesses cabeçalhos.

A tabela a seguir lista as cadeias de caracteres de token iniciais e finais usadas em Tutoriais de exemplo.



| Token | Descrição                      |
|-------|----------------------------------|
| /\*+  | Início do cabeçalho do arquivo                |
| +\*/  | Fim do cabeçalho do arquivo                  |
| /\*-  | Início do cabeçalho de bloco de comentário simples |
| -\*/  | Fim do cabeçalho de bloco de comentário simples   |
| /\*&  | Início do cabeçalho da classe               |
| &\*/  | Fim do cabeçalho de classe                 |
| /\*D  | Início do cabeçalho do método              |
| D\*/  | Fim do cabeçalho do método                |
| /\*Fixo  | Início do cabeçalho da função            |
| Fixo\*/  | Fim do cabeçalho de função              |
| /\*Encontrei  | Início do cabeçalho da interface           |
| Encontrei\*/  | Fim do cabeçalho da interface             |
| /\*Minúscula  | Início do cabeçalho da classe de objeto COM    |
| Minúscula\*/  | Fim do cabeçalho da classe de objeto COM      |



 

Esses cabeçalhos também podem ser usados como indicações visuais para verificação rápida de arquivos de origem. Eles também fornecem conveniência para obter rapidamente um local de origem se você configurar cadeias de caracteres de pesquisa em seu editor e depois repetir a última pesquisa para localizar esses cabeçalhos rapidamente.

Por exemplo, a cadeia de caracteres de pesquisa "M + M" localizará o início dos cabeçalhos de método e "M-M" localizará o início do código de definição/implementação do método real.

 

 




