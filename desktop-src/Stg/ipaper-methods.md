---
title: Métodos IPaper
description: Fornece objetos de copapel que são controlados principalmente por sua interface IPaper nativa.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84153c9fcec021d9084807d73d46198e3a56482
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160355"
---
# <a name="ipaper-methods"></a>Métodos IPaper

O **StoServe** fornece objetos de copapel que são controlados principalmente por sua interface **IPaper** nativa.

A tabela a seguir lista os métodos **IPaper** de IPaper. H no diretório irmão \\ Inc.



| Método    | Descrição                                                         |
|-----------|---------------------------------------------------------------------|
| InitPaper | Inicializa o objeto de papel e cria uma matriz de dados de tinta.                 |
| Bloqueio      | Fornece controle de cliente do papel e bloqueia outros clientes.      |
| Unlock    | Abandona o controle de cliente do documento.                           |
| Carregar      | Carrega o conteúdo em papel do arquivo composto do cliente e notifica os coletores. |
| Salvar      | Salva o conteúdo do papel no arquivo composto do cliente.                      |
| InkStart  | Inicia o desenho de tinta colorida na superfície do papel.                      |
| InkDraw   | Coloca pontos de dados de tinta na superfície de papel eletrônico.               |
| InkStop   | Interrompe o desenho de tinta na superfície do papel.                             |
| Apagar     | Apague o conteúdo do papel atual e notifique os coletores.                 |
| Redimensionar    | Redimensiona o tamanho do retângulo do papel de desenho e notifica os coletores.        |
| Emiti    | Redesenha o conteúdo do objeto de papel e notifica os coletores.                |



 

Os métodos de interesse deste exemplo de código em arquivos compostos são [**carregar**](ipaper--load.md), [**salvar**](ipaper--save.md)e [**redesenhar**](ipaper--redraw.md).

[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) são métodos usados por clientes para o copapel de comando para gravar sequências de desenho de tinta. Normalmente, o cliente responderá a uma \_ mensagem do WM LBUTTONDOWN como o início de uma sequência de desenho de tinta chamando **InkStart** no copaper. À medida que o usuário move o mouse ou a caneta para desenhar enquanto mantém pressionado o botão esquerdo, o cliente responderá às mensagens do WM MOUSEMOVE repetidas \_ com chamadas correspondentes a **InkDraw**. Quando o usuário libera o botão esquerdo do mouse, o cliente responderá a uma \_ mensagem do WM LBUTTONUP com uma chamada para **InkStop**, que marca o final da sequência de desenho de tinta.

[**InkStart**](inkstart-method.md) informa ao copaper a posição inicial da sequência de desenho nas coordenadas da janela do cliente. Ele também passa a cor e a largura da tinta selecionada no momento. O cliente mantém essas seleções; O copaper apenas os registra quando a chamada **InkStart** é feita. [**InkDraw**](inkdraw-method.md) é chamado repetidamente para informar o sucesso das coordenadas da janela que representam o movimento de desenho do mouse ou da caneta. [**InkStop**](cguipaper-methods.md) instrui o copapel para marcar o final de uma sequência de desenho.

 

 




