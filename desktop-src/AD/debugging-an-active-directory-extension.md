---
title: Depurando uma extensão de Active Directory
description: As extensões da folha de propriedades do serviço de diretório do Microsoft Active Directory, do menu de contexto e do assistente de criação de objetos documentadas neste tópico são implementadas como servidores em processamento COM.
ms.assetid: 8c280084-fd2f-4d34-a119-d4e925a68a5c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8d9646f4ccc2e8c740a81ddb48422881744f5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007334"
---
# <a name="debugging-an-active-directory-extension"></a>Depurando uma extensão de Active Directory

As extensões da folha de propriedades do serviço de diretório do Microsoft Active Directory, do menu de contexto e do assistente de criação de objetos documentadas neste tópico são implementadas como servidores em processamento COM. Ou seja, cada extensão é uma DLL que é executada no contexto do processo do host. Para depurar a extensão, é necessário associar a extensão a um aplicativo e executar o aplicativo em um depurador.

## <a name="debugging-active-directory-extensions-displayed-in-the-windows-shell"></a>Depuração de extensões de Active Directory exibidas no Shell do Windows

As extensões de Active Directory exibidas no Shell do Windows são carregadas no contexto do processo de Explorer.exe. Essas extensões podem ser depuradas como uma extensão de shell padrão. Para obter mais informações sobre depuração de extensões do Shell, consulte [Depurando com o Shell](/previous-versions/windows/desktop/legacy/cc144064(v=vs.85)).

## <a name="debugging-active-directory-extensions-displayed-in-the-active-directory-mmc-snap-ins"></a>Extensões de Active Directory de depuração exibidas no Active Directory MMC Snap-Ins

As extensões de Active Directory exibidas nos snap-ins administrativos do MMC do Active Directory são carregadas no contexto do console de gerenciamento Microsoft. Para depurar uma extensão, localize Mmc.exe no sistema local e defina o depurador para usá-lo como o aplicativo para depuração. Na maioria dos sistemas, Mmc.exe está localizado no diretório de sistema do Windows, por exemplo, C: \\ WinNT \\ System32. Dependendo do depurador, você pode ou não precisar definir a DLL de extensão como também sendo carregada pelo depurador. Muitos depuradores também permitem anexar o depurador a um processo do MMC em execução. Para obter mais informações, consulte o guia do usuário do depurador.

Pode ser conveniente fazer com que o MMC carregue automaticamente um snap-in específico. Para fazer isso, defina os argumentos do aplicativo como o caminho e o nome de arquivo de um arquivo MSC. Pode ser um arquivo MSC instalado pelo sistema ou um que você criar. Um arquivo MSC pode ser criado seguindo estas etapas.

1.  Execute Mmc.exe.
2.  Carregue o snap-in desejado selecionando **arquivo**  -  **Adicionar/remover snap-in...** no menu do MMC e selecione o snap-in desejado.
3.  Salve o arquivo MSC selecionando **arquivo**  -  **salvar como...** no menu MMC.

Se você não definir um arquivo MSC de inicialização, deverá carregar manualmente o snap-in desejado ao executar o aplicativo no depurador.

Quando o aplicativo host é executado no depurador, o depurador pode exibir uma mensagem de aviso informando que o aplicativo que está sendo executado não contém nenhum símbolo de depuração. Isso é esperado e pode ser ignorado com segurança porque você está, na verdade, Depurando a DLL, não o aplicativo host.

Na maioria dos casos, a extensão não será chamada até que o usuário execute alguma ação que faça com que a extensão seja carregada e inicializada. Por exemplo, se você estiver Depurando uma extensão de menu de contexto exibida para objetos de usuário, a extensão não será carregada até a primeira vez em que o menu de contexto de um objeto de usuário for exibido.

Agora você deve ser capaz de definir pontos de interrupção e exibir a saída de depuração. Se a extensão não parecer carregar, defina um ponto de interrupção na função [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) da extensão. Se **DllGetClassObject** não for chamado, provavelmente a extensão não está registrada corretamente.

Quando a depuração estiver concluída, saia do MMC e o depurador deverá ser descarregado normalmente.

 

 