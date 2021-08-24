---
description: Para criar uma biblioteca Dynamic-Link dados (DLL), você deve criar um ou mais arquivos de código-fonte e, possivelmente, um arquivo de vinculador para exportar as funções.
ms.assetid: b66ea0e8-84c3-40be-bf02-765b9dd61f9f
title: Dynamic-Link biblioteca de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89047e24fe61483b3ac807b59abc114206a00f9df18566b5fb02947268fbd792
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650446"
---
# <a name="dynamic-link-library-creation"></a>Dynamic-Link biblioteca de dados

Para criar uma biblioteca Dynamic-Link dados (DLL), você deve criar um ou mais arquivos de código-fonte e, possivelmente, um arquivo de vinculador para exportar as funções. Se você planeja permitir que aplicativos que usam sua DLL usem a vinculação dinâmica em tempo de carregamento, você também deve criar uma biblioteca de importação.

## <a name="creating-source-files"></a>Criando arquivos de origem

Os arquivos de origem de uma DLL contêm funções e dados exportados, funções internas e dados e uma função de ponto de entrada opcional [para](dynamic-link-library-entry-point-function.md) a DLL. Você pode usar qualquer ferramenta de desenvolvimento que suporte a criação Windows DLLs baseadas em dados.

Se sua DLL pode ser usada por um aplicativo multithread, você deve tornar sua DLL "thread-safe". Você deve sincronizar o acesso a todos os dados globais da DLL para evitar a corrupção de dados. Você também deve garantir que você vincule apenas com bibliotecas que também são thread-safe. Por exemplo, Microsoft Visual C++ contém várias versões da Biblioteca em Tempo de Executar C, uma que não é thread-safe e duas que são.

## <a name="exporting-functions"></a>Exportando funções

A maneira como você especifica quais funções em uma DLL devem ser exportadas depende das ferramentas que você está usando para desenvolvimento. Alguns compiladores permitem exportar uma função diretamente no código-fonte usando um modificador na declaração de função. Outras vezes, você deve especificar exportações em um arquivo que você passa para o linker.

Por exemplo, usando Visual C++, há duas maneiras possíveis de exportar funções DLL: com o modificador [**\_ \_ declspec(dllexport)**](https://msdn.microsoft.com/library/3y1sfaz2(v=VS.71).aspx) ou com um arquivo de definição de módulo (.def). Se você usar **\_ \_ o modificador declspec(dllexport),** não será necessário usar um arquivo .def. Para obter mais informações, [consulte Exportando de uma DLL](/cpp/build/exporting-from-a-dll?view=vs-2019).

## <a name="creating-an-import-library"></a>Criando uma biblioteca de importação

Um arquivo de biblioteca de importação (.lib) contém informações que o vinculador precisa para resolver referências externas para funções de DLL exportadas, para que o sistema possa localizar a DLL especificada e as funções DLL exportadas em tempo de operação. Você pode criar uma biblioteca de importação para sua DLL ao criar sua DLL.

Para obter mais informações, consulte [Criando uma biblioteca de importação e um arquivo de exportação.](/cpp/build/reference/building-an-import-library-and-export-file?view=vs-2019)

## <a name="using-an-import-library"></a>Usando uma biblioteca de importação

Por exemplo, para chamar a [**função CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) você deve vincular seu código à biblioteca de importação User32.lib. O motivo é que **CreateWindow** reside em uma DLL do sistema chamada User32.dll e User32.lib é a biblioteca de importação usada para resolver as chamadas para funções exportadas em User32.dll em seu código. O linker cria uma tabela que contém o endereço de cada chamada de função. Chamadas para funções em uma DLL serão corrigidas quando a DLL for carregada. Enquanto o sistema está inicializando o processo, ele carrega User32.dll porque o processo depende das funções exportadas nessa DLL e atualiza as entradas na tabela de endereços de função. Todas as chamadas **para CreateWindow** invocam a função exportada de User32.dll.

Para obter informações, [consulte Vinculando implicitamente a uma DLL](/previous-versions/d14wsce5(v=vs.140)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma biblioteca de vínculo dinâmico simples](creating-a-simple-dynamic-link-library.md)
</dt> <dt>

[DLLs (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
