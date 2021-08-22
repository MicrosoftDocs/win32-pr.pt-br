---
title: Como criar exemplos
description: Para criar um exemplo de COM, o ambiente do computador deve ser definido para criar aplicativos C++ do Microsoft Win32.
ms.assetid: c62b8b4d-a9d2-4587-8bb6-7b2c30d1c00d
keywords:
- Como criar exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782a75bb54127191757a515244d439bbff9570c96f4e0bb2ac603477bedb96a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663116"
---
# <a name="how-to-build-samples"></a>Como criar exemplos

Para criar um exemplo de COM, o ambiente do computador deve ser definido para criar aplicativos C++ do Microsoft Win32.

## <a name="preparing-a-computer-to-create-com-samples"></a>Preparando um computador para criar exemplos COM

O ambiente do computador deve ser definido com um compilador C++ de 32 bits instalado corretamente, um linker e um compilador de recursos compatíveis com o Microsoft Visual C++ 4.x ou posterior e um SDK do Windows instalado corretamente. É melhor instalar o SDK Windows último. O Windows SDK fornece arquivos de biblioteca .h include e .lib necessários para a funcionalidade COM codificada nos exemplos.

Para executar com êxito as amostras Remcl euclid, Freserve e Freclhin requer recursos do sistema que estão disponíveis nos sistemas operacionais do Windows: Windows Server 2003, Windows XP, Windows 2000 ou Windows NT 4.0. As amostras Remcl euclid, Freserve e Freclhin serão construídas, mas não serão executados nos sistemas operacionais Windows Me, Windows 98 ou Windows 95, a menos que o COM Distribuído (DCOM) e o COM thread gratuito sejam parte do sistema operacional. Esse suporte está disponível para os sistemas operacionais Windows Me, Windows 98 e Windows 95 no complemento DCOM95. No momento, o DCOM95 pode ser obtido por [download do Microsoft](https://www.microsoft.com/download/details.aspx?id=31661).

Cada diretório de exemplo tem os arquivos de origem necessários para criar e executar o exemplo. O diretório de exemplo pai tem um arquivo Makeall.bat, que você pode executar no prompt de comando para fazer todos os exemplos de código no branch abaixo. Para obter mais informações, consulte o arquivo Makeall.bat dados. Se seu ambiente estiver definido para criar aplicativos C++ win32, você poderá simplesmente executar Makeall.bat no diretório em que ele reside para criar todos os exemplos de código no branch abaixo. Makeall garante a ordem correta para o build para que todas as dependências de exemplo de código sejam atendidas.

O diretório principal também tem um makefile que cria todos os exemplos de código do tutorial usando opções semelhantes às suportadas pelo Makeall.bat. Para obter mais informações, consulte este makefile. Esse makefile presume que todo o branch de exemplos de código está instalado como parte do SDK Windows aplicativo. Atualmente, esse local tem um caminho semelhante a *D: \\ MSSDK \\ SAMPLES \\ COM \\ TUTSAMP,* em que D: representa a unidade de instalação. Se você extraiu o branch de exemplo de código do tutorial (por exemplo, o COM do diretório COM e seus subdireários) para outro local fora do SDK do Windows (ou se você obteve o conjunto de exemplos como um download separado do site da Microsoft), use Makeall.bat para compilar todos os exemplos no branch. Em geral, Makeall.bat é recomendado. Um Logmall.bat também é fornecido. Ele faz o mesmo que o arquivo em lotes Makeall, exceto que registra toda a saída de compilação no arquivo Errorlog.txt no diretório principal do tutorial.

Dois arquivos em lotes, Regall.bat e Unregall.bat, também são fornecidos no diretório principal para registrar e não registrar todos os servidores COM na série de exemplos de código do tutorial. Para registrar todos os servidores, execute Regall.bat arquivo do diretório principal. Para não fazer o registro de todos os servidores, execute Unregall.bat da mesma maneira. Esses arquivos em lotes exigem um build anterior dos exemplos de código REGISTER, MARSHAL, DLLSERVE, LICSERVE, LOCSERVE, APTSERVE, FRESERVE e CONSERVE. Se você executar um build normal dos exemplos de código, os makefiles do servidor registrarão automaticamente os servidores. Nesse caso, não é necessário executar o arquivo em lotes Regall.

Execute o Cleanall.bat em lotes para executar uma Limpeza exaustiva de todos os Exemplos de Tutorial do COM.

> [!WARNING]
> Esse arquivo em lotes exclui todos Visual Studio arquivos de projeto e outros arquivos de trabalho temporários criados por Visual C++ nos exemplos. Todos os servidores COM integrados aos exemplos de código do tutorial não são inscritos no Registro. Todos os arquivos exe e .dll executáveis são excluídos. Todos os arquivos de símbolo de depuração são excluídos. Os arquivos gerados em uma variedade de ambientes de build também são excluídos.

 

Execute 'Makeall Clean' para executar uma limpeza mais rápida, mas mais discreta, de todos os exemplos de código. Essa operação de limpeza não tenta ser tão abrangente quanto a executada pelo Cleanall.bat. Os arquivos .obj são excluídos, mas os binários de saída são mantidos. Os servidores COM não são inscritos no Registro.

Esta série de exemplos originou-se como parte integrante do SDK do Windows, portanto, a narrativa do tutorial assume um ambiente com o SDK Windows instalado corretamente.

No entanto, as versões Microsoft Visual C++ versão 4.0 e posteriores também podem fornecer os arquivos de biblioteca .h include e .lib necessários para compilação. Nesses casos, a instalação do SDK Windows pode não ser necessária para compilar os exemplos.

Para obter mais informações e detalhes completos do build de exemplo, consulte:

[Configuração do ambiente](environment-setup.md)

[Makefiles](makefiles.md)

[Usando o Visual Studio](using-visual-studio.md)

[Extraindo os exemplos de código](extracting-the-code-samples.md)

[Convenções de estilo de codificação](coding-style-conventions.md)

 

 




