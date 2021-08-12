---
description: Visão geral dos exemplos de código da API (interface de programação de aplicativo) para as seções tablet pc e Windows Touch do SDK do Windows.
ms.assetid: 4ede7d0e-e826-4b3a-8a46-0f3162c19cb0
title: Amostras de tablet e toque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cf87ca2cc35da58fe05a72436288413af9f72ecff63a1b2418fb071ca5a025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449779"
---
# <a name="tablet-and-touch-samples"></a>Amostras de tablet e toque

Esta seção contém exemplos que mostram como os aplicativos podem ser desenvolvidos com C, Microsoft Visual Basic .NET e C++ para trabalhar \# com tinta e toque.

Por padrão, os exemplos são instalados em : Exemplos de SDK do Microsoft Tablet PC Platform dos Arquivos de Programas ao instalar <system drive> \\ o \\ \\ \\ SDK do Tablet PC.

> [!Note]  
> Ao instalar o SDK do Windows, o SDK do Windows Server ou o SDK do .NET Framework, os exemplos são instalados no caminho padrão para esse SDK específico.

 

## <a name="available-samples"></a>Exemplos disponíveis



| Amostra                                                                           | Descrição                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reconhecimento Avançado](advanced-recognition-sample.md)                          | Demonstra alguns dos recursos de reconhecimento mais avançados, como a escolha explícita do reconhecedor, factoids e muito mais.<br/>                                                                                                                                                             |
| [Formulário de declarações automáticas](auto-claims-form-sample.md)                                  | Demonstra o uso de dois controles de tinta: o [controle InkEdit](/previous-versions/ms552265(v=vs.100)) e o [controle InkPicture.](/previous-versions/ms583740(v=vs.100))<br/>                                                                                                        |
| [Reconhecimento Básico](basic-recognition-sample.md)                                | Demonstra como criar um aplicativo de reconhecimento de manuscrito simples usando o [objeto RecognizerContext.](/previous-versions/ms828542(v=msdn.10))<br/>                                                                                                                     |
| [Sinks de eventos do C++](c---event-sinks-sample.md)                                    | Demonstra modelos em C++ para todos os eventos da Plataforma de Tablet, que podem ser subclasses ou copiados e copiados e usados como código de modelo.<br/>                                                                                                                                   |
| [Preenchimento automático de caracteres](character-autocomplete-sample.md)                      | Demonstra como implementar o preenchimento automático de caracteres em japonês usando as APIs de reconhecimento.<br/>                                                                                                                                                                                 |
| [Amostra da Web do blog do Ink](ink-blog-web-sample.md)                                   | Demonstra como criar um controle de usuário gerenciado que tem funcionalidade de inking e host que controlam em Internet Explorer<br/>                                                                                                                                                         |
| [Área de Transferência de Tinta](ink-clipboard-sample.md)                                        | Demonstra a interoperabilidade de tinta usando a área de transferência.<br/>                                                                                                                                                                                                                          |
| [Coleção de tinta](ink-collection-sample.md)                                      | Demonstra um aplicativo Windows formulário simples que usa o [objeto InkCollector](/previous-versions/ms583683(v=vs.100)) para coletar tinta.<br/>                                                                                                                                     |
| [Divisor de tinta](ink-divider-sample.md)                                            | Demonstra como usar o objeto [Divisor](/previous-versions/ms839398(v=msdn.10)) para fazer análise de tinta.<br/>                                                                                                                                                                            |
| [Apagamento de tinta](ink-erasing-sample.md)                                            | Demonstra a exclusão de traços de tinta em um aplicativo Windows formulário que usa o [objeto InkCollector](/previous-versions/ms583683(v=vs.100)) para coletar tinta.<br/>                                                                                                             |
| [Teste de acerto de tinta](ink-hit-test-sample.md)                                          | Demonstra duas maneiras de fazer testes de hit ink.<br/>                                                                                                                                                                                                                                       |
| [Reconhecimento de tinta](ink-recognition-sample.md)                                    | Demonstra como você pode criar um aplicativo de reconhecimento de manuscrito simples.<br/>                                                                                                                                                                                                    |
| [Serialização de tinta](ink-serialization-sample.md)                                | Demonstra como serializar a tinta para o formato serializado de tinta (ISF).<br/>                                                                                                                                                                                                           |
| [Exemplo de controle da Web de tinta](ink-web-control-sample.md)                             | Demonstra como criar um controle de tinta para uso em um navegador da Web.<br/>                                                                                                                                                                                                             |
| [Zoom de tinta](ink-zoom-sample.md)                                                  | Demonstra como aplicar zoom corretamente em um aplicativo.<br/>                                                                                                                                                                                                                        |
| [Exemplo de vários reconhecedores](multiple-recognizers-sample.md)                   | Demonstra como selecionar de uma variedade de reconhecedores instalados e, em seguida, usar o reconhecedor selecionado.<br/>                                                                                                                                                                        |
| [Exemplo da Web de implantação sem toque](no-touch-deployment-web-sample.md)             | Demonstra como usar o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para simplificar a entrada de texto em seus aplicativos de formulários. Estende o exemplo de formulário declarações automáticas.<br/>                                                                                      |
| [Peninputpanel](peninputpanel-sample.md)                                        | Demonstra como usar o objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) para simplificar a entrada de texto em seus aplicativos de formulários. Estende o exemplo de formulário declarações automáticas.<br/>                                                                                      |
| [Exemplo de coleção de tinta RealTimeStylus](realtimestylus-ink-collection-sample.md) | Demonstra a coleta de tinta usando a RealTimeStylus.<br/>                                                                                                                                                                                                                           |
| [Exemplo de plug-in RealTimeStylus](realtimestylus-plug-in-sample.md)               | Demonstra como trabalhar com RealTimeStylus.<br/>                                                                                                                                                                                                                                       |
| [Exemplo de formulário de papel digitalizado](scanned-paper-form-sample.md)                       | Demonstra o uso de um formulário verificado em como um bitmap e especificado como a imagem de plano de fundo para um controle [InkPicture](/previous-versions/ms583740(v=vs.100)) sobre a parte superior de um formulário. Várias regiões foram habilitadas para a coleção de tinta (ou, especificada como "inkable").<br/> |
| [Exemplo de informações da plataforma de tablet pc](tablet-pc-platform-info-sample.md)             | Demonstra o uso da função de API de Windows GetSystemMetrics() para determinar se o aplicativo está em execução em um tablet.<br/>                                                                                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de exemplo de DLL do Reconhecedor](recognizer-dll-sample-template.md)
</dt> </dl>

 

