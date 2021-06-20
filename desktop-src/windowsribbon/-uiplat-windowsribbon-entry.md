---
title: Estrutura da faixa de dasgem do Windows
description: Leia uma introdução ao Windows Ribbon Framework, que é uma alternativa moderna para os menus, barras de ferramentas e painéis de tarefas em camadas de aplicativos tradicionais do Windows.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Faixa de-se do Windows
- Faixa de opções
- Documentação da faixa de da Windows
- Documentação da faixa de medida
- API da faixa de medida do Windows
- API da faixa de faixas
- Faixa de Ribbon do Windows, estrutura
- Faixa de Ribbon, estrutura
- Faixa de, sobre o Windows, sobre
- Faixa de, sobre
- Faixa de, componentes do Windows
- Faixa de, componentes
- Faixa de da vista do Windows, exibições
- Faixa de modos, exibições
- Windows Ribbon, arquitetura
- Faixa de faixas, arquitetura
- Windows Ribbon, APIs
- Faixa de das, APIs
- Faixa de das, segurança do Windows
- Faixa de, segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211e1e1cf39a547ad0edbc0c180c62e2f40e15fa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406359"
---
# <a name="windows-ribbon-framework"></a>Estrutura da faixa de dasgem do Windows

O Windows Ribbon Framework é um sistema de apresentação de comando avançado que fornece uma alternativa moderna para os menus, barras de ferramentas e painéis de tarefas em camadas de aplicativos tradicionais do Windows. Semelhante a funcionalidade e aparência à interface do usuário Microsoft Office 2007 Fluent, a estrutura da faixa de tipos é composta por uma barra de comandos da faixa de tipos que expõe os principais recursos de um aplicativo por meio de uma série de guias na parte superior de uma janela de aplicativo e um sistema de menus de contexto.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                           | Descrição                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visões gerais da estrutura da faixa de visão](windowsribbon-overviews-entry.md)<br/>      | Os tópicos contidos nesta seção exploram os conceitos básicos da estrutura da faixa de faixas. <br/>                                                                                                                   |
| [Guias de desenvolvedor da estrutura da faixa de Ribbon](windowsribbon-guides-entry.md)<br/>  | Os tópicos contidos nesta seção descrevem aspectos específicos do Windows Ribbon Framework. <br/>                                                                                                          |
| [Biblioteca de controle da estrutura de faixa](windowsribbon-controls-entry.md)<br/> | Os tópicos contidos nesta seção descrevem o conjunto de controles que estão incluídos com a estrutura da faixa de faixas. Os controles listados aqui são os objetos de interface do usuário em uma faixa de faixas que expõem a funcionalidade do comando.<br/> |
| [Referência da estrutura da faixa de Ribbon](windowsribbon-reference-entry.md)<br/>      | Os tópicos contidos nesta seção fornecem as especificações de referência para a estrutura da faixa de faixas.<br/>                                                                                                       |
| [Amostras da estrutura da faixa de faixas](windowsribbon-samples-entry.md)<br/>          | Os tópicos contidos nesta seção fornecem detalhes sobre os exemplos de código que dão suporte à documentação do Windows Ribbon Framework. <br/>                                                                     |
| [Glossário do Framework da faixa de faixas](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>Público do desenvolvedor

O Windows Ribbon Framework foi projetado para ser usado por desenvolvedores de C/C++ e designers de interface do usuário.

Habilidades recomendadas:

-   Programação COM
-   Programação da API do Windows
-   Programação XML/XAML

Conhecimento básico recomendado:

-   Conceitos de programação da interface do usuário
-   Conceitos gerais da interface do usuário

## <a name="minimum-requirements"></a>Requisitos mínimos



| Requisito | Valor |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte               | Windows 7<br/> Windows Vista com Service Pack 2 (SP2) e [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Servidor mínimo com suporte               | Windows Server 2008 R2<br/> Windows Server 2008 com SP2 e [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows Software Development Kit (SDK) | 7.0                                                                                                                                                                      |
| Cabeçalhos e arquivos IDL                   | uiribbon. h, uiribbon. idl                                                                                                                                                 |



 

> [!Note]  
> A [atualização de plataforma para o Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e [a atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) são conjuntos de bibliotecas de tempo de execução que permitem aos desenvolvedores direcionar aplicativos de faixa de opções do Windows para o Windows Vista e o Windows Server 2008. As atualizações de plataforma estarão disponíveis para todos os clientes do Windows Vista e do Windows Server 2008 por meio do Windows Update. Aplicativos de terceiros que exigem [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) podem ter Windows Update detectar se a atualização necessária está instalada; Se não estiver, Windows Update será baixado e instalado em segundo plano.

 

## <a name="see-also"></a>Consulte Também

[COM (Component Object Model)](../com/component-object-model--com--portal.md)


[API do Windows](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

