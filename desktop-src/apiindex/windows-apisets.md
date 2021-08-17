---
description: Os conjuntos de API são grupos funcionais de APIs win32 no sistema operacional principal. Eles fornecem uma separação de arquitetura da DLL do host na qual uma determinada API do Win32 é definida e o grupo funcional ao qual a API pertence.
title: Windows Conjuntos de API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 34724f255b963c23406ed5bdc59de0278e68a6f75de0d00b4d45aa449575af89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737603"
---
# <a name="windows-api-sets"></a>Windows Conjuntos de API

Todas as versões Windows 10 compartilham uma base comum de componentes do sistema operacional que é chamada de sistema operacional principal *(em* alguns contextos, essa base comum também é *chamada de OneCore*). Nos componentes principais do sistema operacional, as APIs do Win32 são organizadas em grupos funcionais chamados *conjuntos de API.*

A finalidade de um conjunto de API é fornecer uma separação de arquitetura da DLL do host na qual uma determinada API win32 é implementada e o contrato funcional ao qual a API pertence. O desaplamento que os conjuntos de API fornecem entre a implementação e os contratos oferece muitas vantagens de engenharia para desenvolvedores. Em particular, o uso de conjuntos de API em seu código pode melhorar a compatibilidade com todos os Windows 10 dispositivos.

Os conjuntos de API abordam especificamente os seguintes cenários:

- Embora haja suporte para toda a amplitude da API do Win32 em PCs, apenas um subconjunto da API win32 está disponível em outros dispositivos Windows 10, como HoloLens, Xbox e outros dispositivos que executam o Windows 10x. O nome do conjunto de API fornece um mecanismo de consulta para detectar corretamente se uma API está disponível em um determinado dispositivo.

- Algumas implementações de API win32 existem em DLLs com nomes diferentes em diferentes Windows 10 dispositivos. O uso de nomes de conjunto de API em vez de nomes de DLL ao detectar a disponibilidade da API e o carregamento de apIs com atraso fornecem uma rota correta para a implementação, independentemente de onde a API seja realmente implementada.

Para obter mais detalhes, consulte [Operação do carregador do conjunto de API e](api-set-loader-operation.md) Detectar disponibilidade do conjunto de [API.](detect-api-set-availability.md)

## <a name="linking-to-umbrella-libraries"></a>Vinculação a bibliotecas umbrella

Para facilitar a restrição do código às APIs do Win32 com suporte no sistema operacional principal, fornecemos uma série de bibliotecas *umbrella.* Por exemplo, uma biblioteca umbrella chamada OneCore.lib fornece as exportações para o subconjunto de APIs Win32 que são comuns a todos os Windows 10 dispositivos.

As APIs em uma biblioteca umbrella podem ser implementadas em uma variedade de módulos. A biblioteca umbrella abstrai esses detalhes de você, tornando seu código mais portátil entre Windows 10 e dispositivos. Em vez de vincular a bibliotecas como kernel32.lib e advapi32.lib, basta vincular seu aplicativo da área de trabalho ou driver à biblioteca umbrella que contém o conjunto de APIs principais do sistema operacional em que você está interessado.

Para obter mais detalhes, consulte [Windows bibliotecas umbrella](windows-umbrella-libraries.md).

## <a name="api-set-contract-names"></a>Nomes de contrato do conjunto de API

Os conjuntos de API são identificados por um nome de contrato forte que segue essas convenções padrão reconhecidas pelo carregador de biblioteca. 

- O nome deve começar com a cadeia de **caracteres api ou** **ext-**. 
    - Nomes que começam com **api - representam** APIs que têm garantia de existir em todas as Windows 10 versões.
    - Os nomes que começam **com ext-** representam APIs que podem não existir em todas as Windows 10 versões.
- O nome deve terminar com a sequência **l \<n\> - \<n\> - \<n\>**, em que **n** consiste em dígitos decimais.
- O corpo do nome pode ser caracteres alfanuméricos ou traços ( **-** ).
- O nome diferencia maiúsculas de minúsculas.

Aqui estão alguns exemplos de nomes de contrato de conjunto de API:

- **api-ms-win-core-ums-l1-1-0**
- **ext-ms-win-com-ole32-l1-1-5**
- **ext-ms-win-ntuser-window-l1-1-0**
- **ext-ms-win-ntuser-window-l1-1-1**

Você pode usar um nome de conjunto de API no contexto de uma operação do carregador, como [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [P/Invoke,](/dotnet/standard/native-interop/pinvoke) em vez de um nome de módulo DLL para garantir uma rota correta para a implementação, independentemente de onde a API seja realmente implementada no dispositivo atual. No entanto, ao fazer isso, você deve anexar a cadeia **de.dll** no final do nome do contrato. Esse é um requisito do carregador para funcionar corretamente e não é considerado, na verdade, uma parte do nome do contrato. Embora os nomes de contrato pareçam semelhantes aos nomes de DLL nesse contexto, eles são fundamentalmente diferentes dos nomes de módulo DLL e não se referem diretamente a um arquivo no disco.

Exceto para a adoção da cadeia de **caracteres.dll** operações do carregador, os nomes de contrato do conjunto de API devem ser considerados um identificador imutável que corresponde a uma versão de contrato específica.

## <a name="identifying-api-sets-for-win32-apis"></a>Identificando conjuntos de API para APIs do Win32

Para identificar se uma API win32 específica pertence a um conjunto de API, revise a tabela de requisitos na documentação de referência da API. Se a API pertencer a um conjunto de API, a tabela de requisitos no artigo lista o nome do conjunto de API e a Windows na qual a API foi introduzida pela primeira vez no conjunto de API. Para exemplos de APIs que pertencem a um conjunto de API, consulte estes artigos:

- [AllowSetForegroundWindow](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow)
- [FindWindowsEx](/windows/win32/api/winuser/nf-winuser-findwindowexa)
- [Getclassfile](/windows/win32/api/objbase/nf-objbase-getclassfile)

## <a name="in-this-section"></a>Nesta seção

* [Operação de carregador de conjunto de API](api-set-loader-operation.md)
* [Detectar disponibilidade do conjunto de API](detect-api-set-availability.md)
* [Bibliotecas de abrangência do Windows](windows-umbrella-libraries.md)