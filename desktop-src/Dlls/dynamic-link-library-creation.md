---
description: Para criar uma DLL (biblioteca de Dynamic-Link), você deve criar um ou mais arquivos de código-fonte e, possivelmente, um arquivo vinculador para exportar as funções.
ms.assetid: b66ea0e8-84c3-40be-bf02-765b9dd61f9f
title: Criação de biblioteca de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12d296b1494cfcedcdfa823eb1a3dd4d408427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647719"
---
# <a name="dynamic-link-library-creation"></a>Criação de biblioteca de Dynamic-Link

Para criar uma DLL (biblioteca de Dynamic-Link), você deve criar um ou mais arquivos de código-fonte e, possivelmente, um arquivo vinculador para exportar as funções. Se você planeja permitir que os aplicativos que usam sua DLL usem vinculação dinâmica de tempo de carregamento, você também deve criar uma biblioteca de importação.

## <a name="creating-source-files"></a>Criando arquivos de origem

Os arquivos de origem de uma DLL contêm dados e funções exportadas, funções e dados internos e uma [função de ponto de entrada](dynamic-link-library-entry-point-function.md) opcional para a dll. Você pode usar qualquer ferramenta de desenvolvimento que ofereça suporte à criação de DLLs baseadas no Windows.

Se sua DLL pode ser usada por um aplicativo multi-threaded, você deve tornar sua DLL "thread-safe". Você deve sincronizar o acesso a todos os dados globais da DLL para evitar dados corrompidos. Você também deve garantir que você vincule somente com bibliotecas que também são thread-safe. Por exemplo, Microsoft Visual C++ contém várias versões da biblioteca de tempo de execução C, uma que não é thread-safe e duas que são.

## <a name="exporting-functions"></a>Exportando funções

A maneira como você especifica quais funções em uma DLL devem ser exportadas depende das ferramentas que você está usando para desenvolvimento. Alguns compiladores permitem que você exporte uma função diretamente no código-fonte usando um modificador na declaração da função. Em outras ocasiões, você deve especificar as exportações em um arquivo passado para o vinculador.

Por exemplo, usando Visual C++, há duas maneiras possíveis de exportar funções de dll: com o modificador [**\_ \_ declspec (dllexport)**](https://msdn.microsoft.com/library/3y1sfaz2(v=VS.71).aspx) ou com um arquivo de definição de módulo (. def). Se você usar o modificador **\_ \_ declspec (dllexport)** , não será necessário usar um arquivo. def. Para obter mais informações, consulte [exportando de uma DLL](/cpp/build/exporting-from-a-dll?view=vs-2019).

## <a name="creating-an-import-library"></a>Criando uma biblioteca de importação

Um arquivo de biblioteca de importação (. lib) contém informações que o vinculador precisa para resolver referências externas a funções DLL exportadas, para que o sistema possa localizar a DLL especificada e exportar as funções de DLL em tempo de execução. Você pode criar uma biblioteca de importação para sua DLL ao compilar sua DLL.

Para obter mais informações, consulte [criando uma biblioteca de importação e um arquivo de exportação](/cpp/build/reference/building-an-import-library-and-export-file?view=vs-2019).

## <a name="using-an-import-library"></a>Usando uma biblioteca de importação

Por exemplo, para chamar a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) , você deve vincular seu código com a biblioteca de importação user32. lib. O motivo é que a **CreateWindow** reside em uma DLL do sistema chamada User32.dll, e user32. lib é a biblioteca de importação usada para resolver as chamadas para funções exportadas em User32.dll no seu código. O vinculador cria uma tabela que contém o endereço de cada chamada de função. Chamadas para funções em uma DLL serão corrigidas quando a DLL for carregada. Enquanto o sistema está inicializando o processo, ele carrega User32.dll porque o processo depende das funções exportadas nessa DLL e atualiza as entradas na tabela de endereços da função. Todas as chamadas para **CreateWindow** invocam a função exportada de User32.dll.

Para obter informações, consulte [Vinculando implicitamente com uma DLL](/previous-versions/d14wsce5(v=vs.140)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma biblioteca de vínculo dinâmico simples](creating-a-simple-dynamic-link-library.md)
</dt> <dt>

[DLLs (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
