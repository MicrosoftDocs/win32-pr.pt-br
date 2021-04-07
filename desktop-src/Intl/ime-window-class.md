---
description: A classe de janela do IME é uma classe global do sistema predefinida que define a aparência e o comportamento das janelas padrão do IME.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: Classe da janela do IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faae7fd0135ec894186b4e10df9bc02da66bb933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828580"
---
# <a name="ime-window-class"></a>Classe da janela do IME

A classe de janela do IME é uma classe global do sistema predefinida que define a aparência e o comportamento das janelas padrão do IME. A classe é semelhante às classes de controle comuns, pois o aplicativo cria uma janela dessa classe usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Como controles estáticos, uma janela do IME não responde à entrada do usuário por si só. Em vez disso, ele notifica o IME sobre ações de entrada do usuário e processa as mensagens de controle enviadas a ele pelo IME ou pelos aplicativos para executar uma resposta para a ação do usuário.

Os aplicativos com reconhecimento de IME às vezes criam janelas personalizadas do IME usando a classe de janela do IME. O uso da personalização de janelas permite que o aplicativo aproveite o processamento padrão da janela do IME enquanto tem controle do posicionamento da janela.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Gerenciador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 
