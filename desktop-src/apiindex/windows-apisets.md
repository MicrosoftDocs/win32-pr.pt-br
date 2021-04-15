---
description: Os conjuntos de API são grupos funcionais de APIs do Win32 no sistema operacional principal. Eles fornecem uma separação de arquitetura da DLL do host na qual uma determinada API Win32 é definida e o grupo funcional ao qual a API pertence.
title: Conjuntos de API do Windows
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 15c8e6ad8124abf06e6ab3c2a8ca2bcd83772855
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104454482"
---
# <a name="windows-api-sets"></a>Conjuntos de API do Windows

Todas as versões do Windows 10 compartilham uma base comum de componentes do sistema operacional que é chamada de *sistema operacional principal* (em alguns contextos essa base comum também é chamada de *OneCore*). Em componentes do sistema operacional básico, as APIs do Win32 são organizadas em grupos funcionais chamados de *conjuntos de API*.

A finalidade de um conjunto de API é fornecer uma separação de arquitetura da DLL do host em que uma determinada API Win32 é implementada e o contrato funcional ao qual a API pertence. A desassociação que os conjuntos de API fornecem entre a implementação e os contratos oferece muitas vantagens de engenharia para os desenvolvedores. Em particular, o uso de conjuntos de API em seu código pode melhorar a compatibilidade com todos os dispositivos com Windows 10.

Os conjuntos de API abordam especificamente os seguintes cenários:

- Embora a amplitude completa da API do Win32 tenha suporte em PCs, apenas um subconjunto da API do Win32 está disponível em outros dispositivos Windows 10, como o HoloLens, o Xbox e outros dispositivos que executam o Windows 10x. O nome do conjunto de APIs fornece um mecanismo de consulta para detectar corretamente se uma API está disponível em um determinado dispositivo.

- Existem algumas implementações de API do Win32 em DLLs com nomes diferentes em diferentes dispositivos Windows 10. Usar nomes de conjunto de API em vez de nomes de DLL ao detectar disponibilidade de API e atrasar o carregamento de APIs fornece uma rota correta para a implementação, independentemente de onde a API seja realmente implementada.

Para obter mais detalhes, consulte [API Set Loader operação](api-set-loader-operation.md) e [detectar a disponibilidade do conjunto de API](detect-api-set-availability.md).

## <a name="linking-to-umbrella-libraries"></a>Vinculando a bibliotecas de abrangência

Para facilitar a restrição de seu código para as APIs do Win32 com suporte no sistema operacional principal, fornecemos uma série de *bibliotecas de abrangência*. Por exemplo, uma biblioteca abrangente chamada OneCore. lib fornece as exportações para o subconjunto de APIs do Win32 que são comuns a todos os dispositivos Windows 10.

As APIs em uma biblioteca abrangente podem ser implementadas em uma variedade de módulos. A biblioteca de abrangência abstrai esses detalhes, tornando seu código mais portátil em versões e dispositivos do Windows 10. Em vez de vincular a bibliotecas como Kernel32. lib e Advapi32. lib, basta vincular seu aplicativo de área de trabalho ou driver à biblioteca de abrangência que contém o conjunto de APIs do sistema operacional principal em que você está interessado.

Para obter mais detalhes, consulte [bibliotecas de abrangência do Windows](windows-umbrella-libraries.md).

## <a name="api-set-contract-names"></a>Nomes de contrato de conjunto de API

Os conjuntos de API são identificados por um nome de contrato forte que segue essas convenções padrão reconhecidas pelo carregador de biblioteca. 

- O nome deve começar com a cadeia de caracteres **API-** ou **ext-**. 
    - Nomes que começam com **API –** representam APIs que têm garantia de existência em todas as versões do Windows 10.
    - Nomes que começam com **ext-** representam APIs que podem não existir em todas as versões do Windows 10.
- O nome deve terminar com a sequência **l \<n\> - \<n\> - \<n\>**, em que **n** consiste em dígitos decimais.
- O corpo do nome pode ser caracteres alfanuméricos ou traços ( **-** ).
- O nome diferencia maiúsculas de minúsculas.

Aqui estão alguns exemplos de nomes de contrato de conjunto de API:

- **API-MS-Win-Core-ums-L1-1-0**
- **ext-MS-Win-com-Ole32-L1-1-5**
- **ext-MS-Win-Ntuser-Window-L1-1-0**
- **ext-MS-Win-Ntuser-Window-L1-1-1**

Você pode usar um nome de conjunto de API no contexto de uma operação de carregador, como [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [P/Invoke](/dotnet/standard/native-interop/pinvoke) , em vez de um nome de módulo de dll para garantir uma rota correta para a implementação, independentemente de onde a API seja realmente implementada no dispositivo atual. No entanto, ao fazer isso, você deve acrescentar o String **. dll** ao final do nome do contrato. Esse é um requisito do carregador para funcionar corretamente e não é considerado realmente uma parte do nome do contrato. Embora os nomes de contrato sejam semelhantes aos nomes de DLL neste contexto, eles são fundamentalmente diferentes dos nomes de módulo de DLL e não se referem diretamente a um arquivo no disco.

Exceto para acrescentar a String **. dll** em operações de carregador, os nomes de contrato de conjunto de API devem ser considerados um identificador imutável que corresponde a uma versão de contrato específica.

## <a name="identifying-api-sets-for-win32-apis"></a>Identificando conjuntos de API para APIs do Win32

Para identificar se uma determinada API do Win32 pertence a um conjunto de API, examine a tabela de requisitos na documentação de referência da API. Se a API pertencer a um conjunto de API, a tabela de requisitos no artigo listará o nome do conjunto de API e a versão do Windows na qual a API foi introduzida pela primeira vez no conjunto de API. Para obter exemplos de APIs que pertencem a um conjunto de API, consulte estes artigos:

- [AllowSetForegroundWindow](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow)
- [FindWindowsEx](/windows/win32/api/winuser/nf-winuser-findwindowexa)
- [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile)

## <a name="in-this-section"></a>Nesta seção

* [Operação de carregador de conjunto de API](api-set-loader-operation.md)
* [Detectar disponibilidade do conjunto de API](detect-api-set-availability.md)
* [Bibliotecas de abrangência do Windows](windows-umbrella-libraries.md)