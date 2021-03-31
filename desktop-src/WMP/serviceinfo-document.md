---
title: Documento do serviceInfo
description: Documento do serviceInfo
ms.assetid: 48f84dd7-e458-4da2-ae2b-5949e867cd3a
keywords:
- Repositórios online do Windows Media Player, documento do serviceInfo
- repositórios online, documento do serviceInfo
- Digite 1 lojas online, documento do serviceInfo
- tipo 2 lojas online, documento do serviceInfo
- Documento do serviceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539c4e1a58e5dbf88e1fc79909791a7dab767ef1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005167"
---
# <a name="serviceinfo-document"></a>Documento do serviceInfo

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

As lojas online devem criar o documento ServiceInfo.xml. Este é o documento que a loja online usa para configurar a interface do usuário do Windows Media Player quando o Windows Media Player 10 ou posterior está hospedando a loja online.

Os seguintes elementos e seus atributos têm suporte para lojas online do Windows Media Player.



| Elemento                                      | Descrição                                                                                                                                                                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlbumInfo](albuminfo-element.md)           | Especifica a URL para a página da Web que o Windows Media Player exibe quando o usuário escolhe para exibir mais informações sobre um item de mídia específico. Tipo 1: opcional<br/> Tipo 2 música: obrigatório<br/> Comércio do tipo 2: ignorado<br/>                                |
| [ButtonText](buttontext-element.md)         | Especifica a cadeia de texto que o Windows Media Player exibe para um botão de painel de tarefas. Tipo 1: obrigatório<br/> Tipo 2 música: obrigatório<br/> Comércio do tipo 2: obrigatório<br/>                                                                                             |
| [ButtonTip](buttontip-element.md)           | Especifica a dica de ferramenta que é exibida quando o usuário aponta para um botão de painel de tarefas. Tipo 1: opcional<br/> Tipo 2 música: opcional<br/> Comércio do tipo 2: opcional<br/>                                                                                         |
| [BuyCD](buycd-element.md)                   | Especifica as URLs para páginas da Web que o Windows Media Player exibe quando o usuário opta por fazer uma compra. Tipo 1: obrigatório<br/> Tipo 2 música: obrigatório<br/> Comércio do tipo 2: ignorado<br/>                                                                      |
| [Cor](color-element.md)                   | Especifica a cor do plano de fundo para os botões de navegação de lojas online. Tipo 1: opcional<br/> Tipo 2 música: opcional<br/> Comércio do tipo 2: opcional<br/>                                                                                                             |
| [Descrição](description-element.md)       | Especifica uma descrição da loja online que é exibida durante a primeira experiência do usuário com uma instalação do Windows Media Player. Requer o Windows Media Player 11. tipo 1: obrigatório<br/> Tipo 2 música: opcional<br/> Comércio do tipo 2: opcional<br/> |
| [DownloadStatus](downloadstatus-element.md) | Especifica uma URL que o Windows Media Player exibe como um link para permitir que os usuários exibam o status de download. Tipo 1: ignorado<br/> Tipo 2 música: opcional<br/> Comércio do tipo 2: opcional<br/>                                                                         |
| [FriendlyName](friendlyname-element.md)     | Especifica a cadeia de texto que o Windows Media Player exibe para o usuário identificar a loja online. Tipo 1: obrigatório<br/> Tipo 2 música: obrigatório<br/> Comércio do tipo 2: obrigatório<br/>                                                                           |
| [HTMLView](htmlview-element.md)             | Especifica a URL base de uma página da Web HTMLView. Tipo 1: opcional<br/> Tipo 2 música: opcional<br/> Comércio do tipo 2: opcional<br/>                                                                                                                                   |
| [Imagem](image-element.md)                   | Especifica as imagens que o Windows Media Player exibe para o usuário representar a loja online. Tipo 1: obrigatório<br/> Tipo 2 música: opcional<br/> Comércio do tipo 2: opcional<br/>                                                                               |
| [InfoCenter do](infocenter-element.md)         | Especifica a URL da página da Web que o Windows Media Player exibe no recurso de exibição do info Center de **agora em execução** quando o repositório online está ativo. Tipo 1: obrigatório<br/> Tipo 2 música: obrigatório<br/> Comércio do tipo 2: ignorado<br/>                           |
| [Instalar](install-element.md)               | Especifica os valores usados pela instalação do Windows Media Player para instalar o repositório online padrão. Tipo 1: obrigatório<br/> Tipo 2 música: opcional<br/> Comércio do tipo 2: ignorado<br/>                                                                                          |
| [Navegue até](navigate-element.md)             | Especifica uma URL base usada por chamadas para **external. NavigateTaskPaneURL**. Tipo 1: opcional<br/> Tipo 2 música: opcional<br/> Comércio do tipo 2: opcional<br/>                                                                                                          |
| [ServiceInfo](serviceinfo-element.md)       | Representa o elemento principal do documento ServiceInfo.xml. Tipo 1: obrigatório<br/> Tipo 2 música: obrigatório<br/> Comércio do tipo 2: obrigatório<br/>                                                                                                                    |
| [ServiceTask1](servicetask1-element.md)     | Representa o primeiro painel de tarefas da loja online. Tipo 1: obrigatório<br/> Tipo 2 música: obrigatório<br/> Comércio do tipo 2: obrigatório<br/>                                                                                                                                     |
| [ServiceTask2](servicetask2-element.md)     | Representa o segundo painel de tarefas da loja online. Tipo 1: ignorado<br/> Tipo 2 música: opcional<br/> Comércio do tipo 2: opcional<br/>                                                                                                                                     |
| [ServiceTask3](servicetask3-element.md)     | Representa o terceiro painel de tarefas da loja online. Tipo 1: ignorado<br/> Tipo 2 música: opcional<br/> Comércio do tipo 2: opcional<br/>                                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Documento de informações de exemplo para uma loja online tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento de informações de exemplo para uma loja online tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





