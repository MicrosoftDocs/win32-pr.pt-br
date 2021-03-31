---
title: Compilador de MIDL
description: Compilador de MIDL
ms.assetid: ce3d40b7-49fd-4689-9100-fdbad4f0c557
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fa57131e31e9c6273270a771f9ba862d73bc142
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641933"
---
# <a name="midl-compiler"></a>Compilador de MIDL

O compilador MIDL processa um arquivo IDL para gerar uma biblioteca de tipos e arquivos de saída. O tipo de arquivos de saída gerados pelo compilador MIDL depende dos atributos especificados na lista de atributos da interface do arquivo IDL.

Se a lista de atributos contiver a \[ [](/windows/desktop/Midl/object) \] palavra-chave Object, o compilador MIDL gerará arquivos de saída da interface com: um arquivo de proxy de interface, um arquivo de cabeçalho de interface e um arquivo GUID (identificador global exclusivo) para a interface. Se o arquivo IDL contiver uma instrução de [**biblioteca**](/windows/desktop/Midl/library) , MIDL gerará um arquivo de biblioteca de tipos com a extensão de nome de arquivo. tlb. Se houver qualquer interface no arquivo IDL que não tenha a \[  \] palavra-chave Object e não estiver contida em uma instrução de **biblioteca** , o compilador MIDL gerará arquivos de saída de interface apropriados para RPCs (chamadas de procedimento remoto): um arquivo stub de cliente, um arquivo stub de servidor e um arquivo de cabeçalho. Para obter mais informações, consulte os tópicos [definições de interface e bibliotecas de tipos](/windows/desktop/Midl/interface-definitions-and-type-libraries) e [gerando uma biblioteca de tipos com MIDL](/windows/desktop/Midl/generating-a-type-library-with-midl-2).

Para gerar uma biblioteca de tipos e arquivos de saída de um arquivo IDL:

-   No prompt de comando, execute

     *nome de arquivo* MIDL

    em que *filename* é o nome do arquivo IDL.

O compilador MIDL também dá suporte a vários parâmetros opcionais. Para obter uma lista completa, consulte "referência de Command-Line de MIDL" na documentação do Visual C++ ou execute a seguinte linha de comando:

**MIDL/?**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[linguagem IDL da Microsoft](/windows/desktop/Midl/midl-start-page)
</dt> <dt>

[Convertendo para C++](translating-to-c--.md)
</dt> </dl>

 

 