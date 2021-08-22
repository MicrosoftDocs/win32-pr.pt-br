---
title: Usando o Kit de Certificação de Aplicativos Windows
description: para dar ao seu aplicativo de desktop a melhor chance de ser certificado, valide-o e teste-o no seu computador antes de enviá-lo para certificação e listagem na Windows Store.
ms.assetid: 8B460B84-0997-4987-9B66-90F9C6D88D83
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8692e87f8bd152b730129c0d8684bc7ec2ca91964ecd6c25e98eb3db3e0fce44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118708744"
---
# <a name="using-the-windows-app-certification-kit"></a>Usando o Kit de Certificação de Aplicativos Windows

para dar ao seu aplicativo de desktop a melhor chance de ser certificado, valide-o e teste-o no seu computador antes de enviá-lo para certificação e listagem na Windows Store. para certificar seu aplicativo, você precisa instalar e executar o [Kit de certificação de aplicativo Windows](/previous-versions//mt637081(v=vs.85)). para obter detalhes sobre testes específicos no kit, consulte [Windows testes do kit de certificação de aplicativo](windows-app-certification-kit-tests.md).

Para obter uma visão geral do processo de certificação e de onde o uso dessa ferramenta se encaixa, consulte [certificar seu aplicativo de desktop](windows-certification-portal.md).

a versão atual do Windows ACK está disponível em 14 idiomas (tcheco, inglês, francês, alemão, italiano, japonês, coreano, polonês, português (brasil), russo, chinês simplificado, espanhol, chinês tradicional e turco).

## <a name="prerequisites"></a>Pré-requisitos

antes de instalar o Windows ACK, você precisa instalar e executar o sistema operacional.

1. Instale e execute o sistema operacional para o qual você está desenvolvendo aplicativos.

-   se você estiver desenvolvendo aplicativos para o Windows 7, poderá instalar e executar o Windows 7, Windows 8 ou Windows 8.1.
-   se estiver desenvolvendo um aplicativo de área de trabalho Windows 8 ou Windows 8 aplicativo de dispositivo de área de trabalho, você poderá instalar e executar Windows 8 ou Windows 8.1.
-   se você estiver desenvolvendo um aplicativo de área de trabalho Windows 8.1 ou Windows 8 aplicativo de dispositivo de área de trabalho, instale Windows 8.1.

2. instale o [kit de certificação de aplicativo do Windows 3,3](/previous-versions//mt637081(v=vs.85)), que está incluído no Windows Software Development kit (SDK) para Windows 8.1.

**Observação:** ao instalar Windows Kit de certificação de aplicativo 3,3 ou superior em seu computador, você substitui qualquer versão instalada anteriormente do kit.

## <a name="instructions-to-run-windows-app-certification-kit-33"></a>instruções para executar Windows Kit de certificação de aplicativo 3,3

**valide seu aplicativo de desktop usando o Kit de certificação de aplicativo Windows 3,3 interativamente**

1.  na menu Iniciar, pesquise por Windows Kit de certificado de aplicativo.
2.  no Kit de certificação de aplicativo Windows, clique na categoria validação de teste que você deseja executar. Se você estiver validando um aplicativo de área de trabalho, selecione **validar aplicativo de área de trabalho**.
3.  Na próxima tela, navegue até o arquivo de instalação do aplicativo de desktop que você deseja validar.
    -   **Observação:** Você pode usar as [etapas da linha de comando](#commandlinesteps) para incluir opções ou uma opção de instalação, se necessário.
4.  Indique o tipo de uso do aplicativo e clique em **Avançar**. o Kit de certificação de aplicativo Windows começa a instalar o aplicativo de desktop usando os arquivos de instalação para que ele possa validar a instalação.
5.  Se for solicitado que você reinicialize o sistema para concluir a instalação, escolha **não**. Se seu aplicativo precisar instalar vários componentes ou dependências externas, selecione cuidadosamente o nome do seu aplicativo. o nome escolhido aqui é o nome que seu aplicativo receberá se ele for listado no repositório de Windows. Quando a validação for concluída, salve o relatório com o nome que você deu a seu aplicativo na etapa 6. o Kit de certificação de aplicativo Windows cria um arquivo de relatório XML e o salva.
6.  Navegue até a pasta em que você salvou o relatório e abra-o para exibir os resultados do teste. Se o teste falhou e você está qualificado para uma renúncia, as informações que você precisa enviar estão listadas aqui. Você deve enviar uma descrição detalhada para cada solicitação de renúncia possível.

**validar seu aplicativo de área de trabalho Windows usando o Kit de certificação de aplicativo do Windows 3,3 de uma linha de comando**

1.  Navegue até a pasta em que você salvou o relatório e abra-o para exibir os resultados do teste. Os testes com falha com uma possível solicitação de renúncia estão listados aqui. Você deve enviar uma descrição detalhada para cada solicitação de renúncia possível.
2.  na pasta que contém o Kit de certificação de aplicativo Windows, insira estes comandos nesta ordem:

    -   <span id="commandLineSteps"></span><span id="commandlinesteps"></span><span id="COMMANDLINESTEPS"></span>`appcert.exe reset`
    -   `appcert test -apptype desktop -setuppath d:\cdrom\setup.exe  -appusage peruser -reportoutputpath [report file name]`

    Onde: `[report file name]` é o nome de arquivo totalmente qualificado do arquivo XML que o kit criará para conter o relatório de teste.

3.  Após a conclusão do teste, abra o arquivo de relatório chamado \[ nome \] do arquivo de relatório e exiba os resultados do teste.

    **Observação:** para obter mais informações sobre a linha de comando do Kit de certificação de aplicativo Windows, digite o comando appcert.exe/?

    o Kit de certificação de aplicativo Windows deve ser executado no contexto de uma sessão de usuário ativa, mas você não pode iniciar aplicativos em uma sessão não interativa. A maneira como o kit manipula tokens para executar testes com ou sem privilégios administrativos depende também desse contexto de sessão de usuário. O kit pode ser executado de um serviço, mas o serviço deve ser capaz de gerar o processo do kit em uma sessão de usuário ativa.

**Use o Kit de certificação de aplicativo Windows para validar seus aplicativos Windows 7**

-   o kit de certificação de aplicativos Windows substituiu o Windows kit de logotipo de Software. se você quiser o logotipo do Windows 7 para seu aplicativo, use o Kit de certificação de aplicativo Windows para seu relatório e teste de validação. o kit pode detectar em qual sistema operacional ele está sendo executado e é iniciado automaticamente para aplicativos Windows 7. siga o mesmo processo para validar aplicativos Windows 7.

**Enviar para certificação**

-   Depois que seu aplicativo for validado, você estará pronto para enviá-lo para [a certificação por meio do processo de envio do portal](https://www.microsoft.com/?ref=go).

## <a name="reference-documents"></a>Documentos de referência

-   [requisitos de certificação para aplicativos da área de trabalho Windows](/windows/desktop/win_cert/certification-requirements-for-windows-desktop-apps)
-   [white paper de certificação de aplicativo](https://www.microsoft.com/download/details.aspx?id=27414)
-   [Windows Integração da loja para aplicativos da área de trabalho](/previous-versions//dn322034(v=vs.85))
-   [requisitos de certificação de aplicativo de desktop Windows 7](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)

## <a name="windows-app-certification-kit-tests"></a>Testes do Kit de Certificação de Aplicativos Windows

alteramos o kit para facilitar o uso dos [testes Windows ACK](windows-app-certification-kit-tests.md) . O kit agora tem:

-   Uma nova interface do usuário simplificada
-   Teste de vários usuários aprimorado, que não exige mais que você configure uma segunda conta de usuário

 

 