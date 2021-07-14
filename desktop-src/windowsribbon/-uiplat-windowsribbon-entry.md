---
title: Windows Estrutura da faixa de faixas
description: leia uma introdução ao Windows estrutura da faixa de opção, que é uma alternativa moderna aos menus, barras de ferramentas e painéis de tarefas em camadas de aplicativos tradicionais de Windows.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Windows 3D
- Faixa de opções
- Windows Documentação da faixa de medida
- Documentação da faixa de medida
- Windows API da faixa de faixas
- API da faixa de faixas
- Windows Faixa de Ribbon, estrutura
- Faixa de Ribbon, estrutura
- Windows Faixa de, sobre
- Faixa de, sobre
- Windows Faixa de, componentes
- Faixa de, componentes
- Windows Faixa de modos, exibições
- Faixa de modos, exibições
- Windows Faixa de faixas, arquitetura
- Faixa de faixas, arquitetura
- Windows Faixa de das, APIs
- Faixa de das, APIs
- Windows Faixa de, segurança
- Faixa de, segurança
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 98f7dbf42d604f93c76bb9897aa25918d45d126f
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691645"
---
# <a name="windows-ribbon-framework"></a>Windows Estrutura da faixa de faixas

o Windows estrutura da faixa de opção é um sistema de apresentação de comando avançado que fornece uma alternativa moderna para os menus, barras de ferramentas e painéis de tarefas em camadas de aplicativos tradicionais de Windows. semelhante na funcionalidade e na aparência à interface do usuário do Microsoft Office 2007 Fluent, a estrutura da faixa de tipos é composta por uma barra de comandos da faixa de tipos que expõe os principais recursos de um aplicativo por meio de uma série de guias na parte superior de uma janela do aplicativo e um sistema de menus de contexto.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                           | Descrição                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visões gerais da estrutura da faixa de visão](windowsribbon-overviews-entry.md)<br/>      | Os tópicos contidos nesta seção exploram os conceitos básicos da estrutura da faixa de faixas. <br/>                                                                                                                   |
| [Guias de desenvolvedor da estrutura da faixa de Ribbon](windowsribbon-guides-entry.md)<br/>  | os tópicos contidos nesta seção descrevem aspectos específicos do Windows estrutura da faixa de informações. <br/>                                                                                                          |
| [Biblioteca de controle da estrutura de faixa](windowsribbon-controls-entry.md)<br/> | Os tópicos contidos nesta seção descrevem o conjunto de controles que estão incluídos com a estrutura da faixa de faixas. Os controles listados aqui são os objetos de interface do usuário em uma faixa de faixas que expõem a funcionalidade do comando.<br/> |
| [Referência da estrutura da faixa de Ribbon](windowsribbon-reference-entry.md)<br/>      | Os tópicos contidos nesta seção fornecem as especificações de referência para a estrutura da faixa de faixas.<br/>                                                                                                       |
| [Amostras da estrutura da faixa de faixas](windowsribbon-samples-entry.md)<br/>          | os tópicos contidos nesta seção fornecem detalhes sobre os exemplos de código que dão suporte à documentação do Windows Ribbon framework. <br/>                                                                     |
| [Glossário do Framework da faixa de faixas](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>Público do desenvolvedor

o Windows estrutura da faixa de d ' foi projetado para ser usado por desenvolvedores de C/C++ e designers de interface do usuário.

Habilidades recomendadas:

- Programação COM
- Windows Programação de API
- Programação XML/XAML

Conhecimento básico recomendado:

- Conceitos de programação da interface do usuário
- Conceitos gerais da interface do usuário

## <a name="minimum-requirements"></a>Requisitos mínimos



| Requisito | Valor |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte               | Windows 7<br/> Windows vista com Service Pack 2 (SP2) e [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Servidor mínimo com suporte               | Windows Server 2008 R2<br/> Windows servidor 2008 com SP2 e [atualização de plataforma para o Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows Software Development Kit (SDK) | 7.0                                                                                                                                                                      |
| Cabeçalhos e arquivos IDL                   | uiribbon. h, uiribbon. idl                                                                                                                                                 |



 

> [!Note]  
> a [atualização de plataforma para o Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e [a atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) são conjuntos de bibliotecas de tempo de execução que permitem aos desenvolvedores direcionar Windows aplicativos de faixa de opções para o Windows Vista e o Windows Server 2008. as atualizações de plataforma estarão disponíveis para todos os clientes Windows Vista e Windows Server 2008 por meio do Windows Update. aplicativos de terceiros que exigem [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) podem ter Windows Update detectar se a atualização necessária está instalada; se não estiver, Windows Update será baixado e instalado em segundo plano.

 

## <a name="see-also"></a>Consulte Também

[COM (Component Object Model)](../com/component-object-model--com--portal.md)


[API do Windows](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

