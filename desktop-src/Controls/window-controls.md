---
title: Controles do Windows
description: Um controle é uma janela filho que um aplicativo usa em conjunto com outra janela para habilitar a interação do usuário.
ms.assetid: 0a6eb481-d94e-40c5-afec-46354520f08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bf14f3c93f6f38ba787cba463977a4dca9eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005123"
---
# <a name="windows-controls"></a>Controles do Windows

## <a name="purpose"></a>Finalidade

Um controle é uma janela filho que um aplicativo usa em conjunto com outra janela para habilitar a interação do usuário. Os controles são usados com mais frequência nas caixas de diálogo, mas também podem ser usados em outras janelas. Os controles nas caixas de diálogo fornecem ao usuário uma maneira de digitar texto, escolher opções e iniciar ações. Os controles em outras janelas fornecem uma variedade de serviços, como permitir que o usuário escolha comandos, Exibir status e exibir e editar texto. Esta documentação descreve os controles fornecidos pelo Windows e os elementos de programação usados para criá-los e manipulá-los.

Para obter uma lista de todos os controles do Windows, incluindo um link para uma visão geral abrangente e informações de referência para cada controle, consulte [Control library](individual-control-info.md).

## <a name="developer-audience"></a>Público de desenvolvedores

Os controles são projetados para uso por desenvolvedores de C/C++ e designers de interface do usuário. Em geral, os desenvolvedores precisam de um nível moderado de compreensão sobre conceitos de programação de interface do usuário, programação de API do Windows e Unicode.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O suporte para controles é fornecido por User32.dll e Comctl32.dll. Para obter mais informações, consulte [versões de controle comuns](common-control-versions.md).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                             | Descrição                                                                                                                                     |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre controles comuns](common-controls-intro.md)<br/>                     | Fornece informações gerais que são comuns a todos os controles com suporte pelo Comctl32.dll.<br/>                                      |
| [Mensagens de controle](control-messages.md)<br/>                               | Explica como as mensagens do Windows são usadas para se comunicar com controles.<br/>                                                                 |
| [Controles personalizados](user-controls-intro.md)<br/>                             | Descreve várias maneiras de criar controles personalizados. <br/>                                                                                 |
| [Controles de subclasses](subclassing-overview.md)<br/>                       | Descreve uma maneira de personalizar um controle alterando seus recursos ou adicionando novos. <br/>                                                 |
| [Desenho personalizado](custom-draw.md)<br/>                                         | Descreve um serviço, fornecido por alguns controles, que os aplicativos podem usar para personalizar vários aspectos da aparência do controle. <br/> |
| [Considerações de segurança: controles do Microsoft Windows](sec-comctls.md)<br/> | Fornece informações sobre considerações de segurança relacionadas aos controles do Windows. <br/>                                                 |
| [Biblioteca de controles](individual-control-info.md)<br/>                         | Fornece visões gerais e informações de referência sobre cada controle com suporte pelo User32.dll e Comctl32.dll.<br/>                            |
| [Referência de controle geral](common-control-reference.md)<br/>              | Fornece informações de referência sobre elementos de programação que se aplicam a vários controles, não apenas a um controle específico.<br/>           |
| [Controle Spy v 2.0](control-spy.md)<br/>                                    | Descreve o Spy Control, uma ferramenta que ajuda os desenvolvedores a entenderem os controles comuns. <br/>                                                     |
| [Estilos visuais](themes-overview.md)<br/>                                   | Descreve como a aparência dos controles pode ser alterada dependendo do estilo visual escolhido pelo usuário. <br/>                               |
| [Formato de arquivo de tema](themesfileformat-overview.md)<br/>                     | Discute o formato dos arquivos de tema (. Theme) usados no Windows 7 e no Windows Vista.<br/>                                                    |



 

 

 





