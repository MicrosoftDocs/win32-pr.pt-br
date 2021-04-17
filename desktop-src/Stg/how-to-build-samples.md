---
title: Como criar amostras
description: Para criar um exemplo de COM, o ambiente de computador deve ser configurado para criar aplicativos do Microsoft Win32 C++.
ms.assetid: c62b8b4d-a9d2-4587-8bb6-7b2c30d1c00d
keywords:
- Como criar amostras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593d3465d3ebcc32a6768dd8b2dffe1f0a653d07
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "105754929"
---
# <a name="how-to-build-samples"></a>Como criar amostras

Para criar um exemplo de COM, o ambiente de computador deve ser configurado para criar aplicativos do Microsoft Win32 C++.

## <a name="preparing-a-computer-to-create-com-samples"></a>Preparando um computador para criar amostras COM

O ambiente de computador deve ser configurado com um compilador C++ de 32 bits, vinculador e recurso instalado corretamente que seja compatível com o Microsoft Visual C++ 4. x ou posterior e um SDK do Windows instalado corretamente. É melhor instalar o SDK do Windows por último. O SDK do Windows fornece os arquivos de biblioteca. h include e. lib necessários para a funcionalidade COM codificada nos exemplos.

Para executar com êxito os exemplos de Remclien, Freserve e Freclien exigem os recursos do sistema que estão disponíveis nos sistemas operacionais Windows: Windows Server 2003, Windows XP, Windows 2000 ou Windows NT 4,0. Os exemplos de Remclien, Freserve e Freclien serão criados, mas não serão executados nos sistemas operacionais Windows me, Windows 98 ou Windows 95, a menos que Distributed COM (DCOM) e COM threaded COM sejam parte do sistema operacional. Esse suporte está disponível para os sistemas operacionais Windows me, Windows 98 e Windows 95 no complemento do DCOM95. Atualmente, o DCOM95 pode ser obtido pelo [download da Microsoft](https://www.microsoft.com/download/details.aspx?id=31661).

Cada diretório de exemplo tem os arquivos de origem necessários para compilar e executar o exemplo. O diretório de exemplo pai tem um arquivo Makeall.bat, que pode ser executado no prompt de comando para disponibilizar todos os exemplos de código na ramificação. Para obter mais informações, consulte o arquivo Makeall.bat. Se o seu ambiente estiver configurado para criar aplicativos Win32 C++, você poderá simplesmente executar Makeall.bat do diretório em que ele reside para criar todos os exemplos de código na ramificação abaixo. O Makeall garante a ordem correta para a compilação para que todas as dependências de exemplo de código sejam satisfeitas.

O diretório principal também tem um makefile que cria todos os exemplos de código do tutorial usando opções semelhantes àquelas com suporte pelo Makeall.bat. Para obter mais informações, consulte este makefile. Esse makefile pressupõe que toda a ramificação de exemplos de código seja instalada como parte do SDK do Windows. Atualmente, esse local tem um caminho semelhante a *d: \\ MSSDK \\ Samples \\ com \\ TUTSAMP*, em que D: representa a unidade de instalação. Se você tiver extraído a ramificação de exemplo de código do tutorial (por exemplo, o COM do diretório COM e seus subdiretórios) para outro local fora do SDK do Windows (ou se você tiver obtido o conjunto de exemplo como um download separado do site da Microsoft), use Makeall.bat para compilar todos os exemplos na ramificação. Em geral, é recomendável Makeall.bat. Um arquivo de Logmall.bat também é fornecido. Ele faz o mesmo que o arquivo em lote Makeall, exceto que ele registra em log toda a saída de compilação no arquivo Errorlog.txt no diretório principal do tutorial.

Dois arquivos em lotes, Regall.bat e Unregall.bat, também são fornecidos no diretório principal para registrar e cancelar o registro de todos os servidores COM na série de exemplos de código do tutorial. Para registrar todos os servidores, execute Regall.bat arquivo do diretório principal. Para cancelar o registro de todos os servidores, execute Unregall.bat da mesma maneira. Esses arquivos em lotes exigem uma compilação anterior dos exemplos de código REGISTER, MARSHAL, DLLSERVE, LICSERVE, LOCSERVE, APTSERVE, FRESERVE e preserve. Se você executar uma compilação normal dos exemplos de código, os makefiles do servidor registrarão automaticamente os servidores. Nesse caso, não é necessário executar o arquivo em lotes Regall.

Execute o arquivo em lote Cleanall.bat para executar uma Cleanall exaustiva de todos os exemplos de tutorial COM.

> [!WARNING]
> Esse arquivo em lotes exclui todos os arquivos de projeto do Visual Studio e outros arquivos de trabalho temporários criados por Visual C++ nos exemplos. Todos os servidores COM criados nos exemplos de código do tutorial são desregistrados do registro. Todos os arquivos exe e. dll executáveis são excluídos. Todos os arquivos de símbolo de depuração são excluídos. Os arquivos gerados em uma variedade de ambientes de compilação também são excluídos.

 

Execute ' Makeall Clean ' para executar uma limpeza mais rápida, mas mais modesto, de todos os exemplos de código. Essa operação de limpeza não tenta ser tão abrangente quanto a realizada pelo Cleanall.bat. Os arquivos. obj são excluídos, mas os binários de saída são retidos. Os servidores COM não estão registrados no registro.

Essa série de exemplo foi originada como parte integrante do SDK do Windows, portanto, a narração do tutorial pressupõe um ambiente com o SDK do Windows instalado corretamente.

No entanto, as versões do Microsoft Visual C++ versão 4,0 e posterior também podem fornecer os arquivos de biblioteca. h include e. lib necessários para a compilação. Nesses casos, a instalação do SDK do Windows pode não ser necessária para compilar os exemplos.

Para obter mais informações e detalhes de compilação de exemplo completos, consulte:

[Configuração do ambiente](environment-setup.md)

[Makefiles](makefiles.md)

[Usando o Visual Studio](using-visual-studio.md)

[Extraindo os exemplos de código](extracting-the-code-samples.md)

[Convenções de estilo de codificação](coding-style-conventions.md)

 

 




