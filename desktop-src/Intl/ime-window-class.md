---
description: A classe de janela IME é uma classe global do sistema predefinida que define a aparência e o comportamento das janelas padrão do IME.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: Classe de janela IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56449534467a2b01ce8e59991bfc1c5f5ad4e1a9156f86cee5e154a8b8eb1d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107186"
---
# <a name="ime-window-class"></a>Classe de janela IME

A classe de janela IME é uma classe global do sistema predefinida que define a aparência e o comportamento das janelas padrão do IME. A classe é semelhante às classes de controle comuns em que o aplicativo cria uma janela dessa classe usando a [**função CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Assim como os controles estáticos, uma janela do IME não responde à entrada do usuário por si só. Em vez disso, ele notifica o IME de ações de entrada do usuário e processa mensagens de controle enviadas a ele pelo IME ou aplicativos para executar uma resposta à ação do usuário.

Aplicativos com IME às vezes criam janelas IME personalizadas usando a classe de janela IME. O uso da personalização de janela permite que o aplicativo aproveite o processamento padrão da janela IME enquanto tem controle do posicionamento da janela.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciador de Métodos de Entrada](about-input-method-manager.md)
</dt> </dl>

 

 
