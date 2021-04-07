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
# <a name="ime-window-class"></a><span data-ttu-id="5384b-103">Classe da janela do IME</span><span class="sxs-lookup"><span data-stu-id="5384b-103">IME Window Class</span></span>

<span data-ttu-id="5384b-104">A classe de janela do IME é uma classe global do sistema predefinida que define a aparência e o comportamento das janelas padrão do IME.</span><span class="sxs-lookup"><span data-stu-id="5384b-104">The IME window class is a predefined system global class that defines the appearance and behavior of the standard IME windows.</span></span> <span data-ttu-id="5384b-105">A classe é semelhante às classes de controle comuns, pois o aplicativo cria uma janela dessa classe usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="5384b-105">The class is similar to common control classes in that the application creates a window of this class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="5384b-106">Como controles estáticos, uma janela do IME não responde à entrada do usuário por si só.</span><span class="sxs-lookup"><span data-stu-id="5384b-106">Like static controls, an IME window does not respond to user input by itself.</span></span> <span data-ttu-id="5384b-107">Em vez disso, ele notifica o IME sobre ações de entrada do usuário e processa as mensagens de controle enviadas a ele pelo IME ou pelos aplicativos para executar uma resposta para a ação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5384b-107">Instead, it notifies the IME of user input actions and processes control messages sent to it by the IME or applications to carry out a response to the user action.</span></span>

<span data-ttu-id="5384b-108">Os aplicativos com reconhecimento de IME às vezes criam janelas personalizadas do IME usando a classe de janela do IME.</span><span class="sxs-lookup"><span data-stu-id="5384b-108">IME-aware applications sometimes create customized IME windows using the IME window class.</span></span> <span data-ttu-id="5384b-109">O uso da personalização de janelas permite que o aplicativo aproveite o processamento padrão da janela do IME enquanto tem controle do posicionamento da janela.</span><span class="sxs-lookup"><span data-stu-id="5384b-109">Use of window customization allows the application to take advantage of the default processing of the IME window while having control of window positioning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5384b-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5384b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5384b-111">Sobre o Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="5384b-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
