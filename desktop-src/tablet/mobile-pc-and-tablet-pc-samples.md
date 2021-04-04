---
description: Visão geral dos exemplos de código da API (interface de programação de aplicativo) para as seções do Tablet PC e do Windows Touch do SDK do Windows.
ms.assetid: 4ede7d0e-e826-4b3a-8a46-0f3162c19cb0
title: Exemplos de Tablet e toque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8562dcc1baa42f44d6ca675344d658b1bf693cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837345"
---
# <a name="tablet-and-touch-samples"></a>Exemplos de Tablet e toque

Esta seção contém exemplos que mostram como os aplicativos podem ser desenvolvidos com o C \# , o Microsoft Visual Basic .net e o C++ para trabalhar com tinta e toque.

Por padrão, os exemplos são instalados em <system drive> : \\ arquivos de programas \\ Microsoft Tablet PC Platform SDK \\ Samples \\ ao instalar o SDK do Tablet PC.

> [!Note]  
> Ao instalar o SDK do Windows, o SDK do Windows Server ou o SDK do .NET Framework, os exemplos são instalados no caminho padrão para esse SDK específico.

 

## <a name="available-samples"></a>Exemplos disponíveis



| Amostra                                                                           | Descrição                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reconhecimento avançado](advanced-recognition-sample.md)                          | Demonstra alguns dos recursos de reconhecimento mais avançados, como escolha explícita do reconhecedor, factos e muito mais.<br/>                                                                                                                                                             |
| [Formulário de declarações automáticas](auto-claims-form-sample.md)                                  | Demonstra o uso de dois controles de tinta: o controle [InkEdit](/previous-versions/ms552265(v=vs.100)) e o controle [InkPicture](/previous-versions/ms583740(v=vs.100)) .<br/>                                                                                                        |
| [Reconhecimento básico](basic-recognition-sample.md)                                | Demonstra como criar um aplicativo de reconhecimento de manuscrito simples, usando o objeto [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) .<br/>                                                                                                                     |
| [Coletores de eventos C++](c---event-sinks-sample.md)                                    | Demonstra modelos em C++ para todos os eventos da plataforma Tablet, que podem ser subclassedos ou copiados e colados e usados como código de modelo.<br/>                                                                                                                                   |
| [Preenchimento automático de caracteres](character-autocomplete-sample.md)                      | Demonstra como implementar o preenchimento automático de caracteres em Japonês usando as APIs de reconhecimento.<br/>                                                                                                                                                                                 |
| [Exemplo da Web do blog de tinta](ink-blog-web-sample.md)                                   | Demonstra como criar um controle de usuário gerenciado que tem capacidade de escrita a tinta e hospedar esse controle no Internet Explorer<br/>                                                                                                                                                         |
| [Área de transferência de tinta](ink-clipboard-sample.md)                                        | Demonstra a interoperabilidade de tinta usando a área de transferência.<br/>                                                                                                                                                                                                                          |
| [Coleta de tinta](ink-collection-sample.md)                                      | Demonstra um aplicativo simples do Windows Form que usa o objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para coletar tinta.<br/>                                                                                                                                     |
| [Divisória de tinta](ink-divider-sample.md)                                            | Demonstra como usar o objeto [divisória](/previous-versions/ms839398(v=msdn.10)) para fazer a análise de tinta.<br/>                                                                                                                                                                            |
| [Apagamento de tinta](ink-erasing-sample.md)                                            | Demonstra a exclusão de traços de tinta em um aplicativo do Windows Form que usa o objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para coletar tinta.<br/>                                                                                                             |
| [Teste de colisão de tinta](ink-hit-test-sample.md)                                          | Demonstra duas maneiras de testar a tinta.<br/>                                                                                                                                                                                                                                       |
| [Reconhecimento de tinta](ink-recognition-sample.md)                                    | Demonstra como você pode criar um aplicativo de reconhecimento de manuscrito simples.<br/>                                                                                                                                                                                                    |
| [Serialização de tinta](ink-serialization-sample.md)                                | Demonstra como serializar a tinta para o formato serializado da tinta (ISF).<br/>                                                                                                                                                                                                           |
| [Exemplo de controle da Web de tinta](ink-web-control-sample.md)                             | Demonstra como criar um controle de tinta para uso em um navegador da Web.<br/>                                                                                                                                                                                                             |
| [Zoom de tinta](ink-zoom-sample.md)                                                  | Demonstra como aplicar zoom à tinta em um aplicativo corretamente.<br/>                                                                                                                                                                                                                        |
| [Exemplo de vários reconhecedores](multiple-recognizers-sample.md)                   | Demonstra como selecionar de uma variedade de reconhecedores instalados e, em seguida, usar o reconhecedor selecionado.<br/>                                                                                                                                                                        |
| [Exemplo de Web de implantação não Touch](no-touch-deployment-web-sample.md)             | Demonstra como usar o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para tornar a entrada de texto em seus aplicativos de formulários mais simples. Estende o exemplo de formulário de declarações automáticas.<br/>                                                                                      |
| [PenInputPanel](peninputpanel-sample.md)                                        | Demonstra como usar o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para tornar a entrada de texto em seus aplicativos de formulários mais simples. Estende o exemplo de formulário de declarações automáticas.<br/>                                                                                      |
| [Exemplo de coleção de tinta do RealTimeStylus](realtimestylus-ink-collection-sample.md) | Demonstra a coleta de tinta usando o RealTimeStylus.<br/>                                                                                                                                                                                                                           |
| [Exemplo de plug-in RealTimeStylus](realtimestylus-plug-in-sample.md)               | Demonstra como trabalhar com o RealTimeStylus.<br/>                                                                                                                                                                                                                                       |
| [Exemplo de formulário de papel digitalizado](scanned-paper-form-sample.md)                       | Demonstra o uso de um formulário digitalizado como um bitmap e especificado como a imagem de plano de fundo para um controle [InkPicture](/previous-versions/ms583740(v=vs.100)) na parte superior de um formulário. Várias regiões foram habilitadas para a coleção de tinta (ou, especificada como "inkable").<br/> |
| [Exemplo de informações sobre a plataforma do Tablet PC](tablet-pc-platform-info-sample.md)             | Demonstra o uso da função de API do Windows GetSystemMetrics () para determinar se o aplicativo está sendo executado em um Tablet PC.<br/>                                                                                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de exemplo de DLL do Recognizer](recognizer-dll-sample-template.md)
</dt> </dl>

 

