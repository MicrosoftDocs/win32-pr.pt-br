---
title: Usando o Kit de Certificação de Aplicativos Windows
description: Para dar ao seu aplicativo de desktop a melhor chance de ser certificado, valide-o e teste-o no seu computador antes de enviá-lo para certificação e listagem na Windows Store.
ms.assetid: 8B460B84-0997-4987-9B66-90F9C6D88D83
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89b3c6e4de3286dd6418c4c8e186bcadaddf00b7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366827"
---
# <a name="using-the-windows-app-certification-kit"></a>Usando o Kit de Certificação de Aplicativos Windows

Para dar ao seu aplicativo de desktop a melhor chance de ser certificado, valide-o e teste-o no seu computador antes de enviá-lo para certificação e listagem na Windows Store. Para certificar seu aplicativo, você precisa instalar e executar o [Kit de certificação de aplicativos para Windows](/previous-versions//mt637081(v=vs.85)). Para obter detalhes sobre testes específicos no kit, consulte [testes do kit de certificação de aplicativos para Windows](windows-app-certification-kit-tests.md).

Para obter uma visão geral do processo de certificação e de onde o uso dessa ferramenta se encaixa, consulte [certificar seu aplicativo de desktop](windows-certification-portal.md).

A versão atual do Windows ACK está disponível em 14 idiomas (tcheco, inglês, francês, alemão, italiano, japonês, coreano, polonês, Português (Brasil), russo, chinês simplificado, espanhol, chinês tradicional e turco).

## <a name="prerequisites"></a>Pré-requisitos

Antes de instalar o Windows ACK, você precisa instalar e executar o sistema operacional.

1. Instale e execute o sistema operacional para o qual você está desenvolvendo aplicativos.

-   Se você estiver desenvolvendo aplicativos para o Windows 7, poderá instalar e executar o Windows 7, Windows 8 ou Windows 8.1.
-   Se você estiver desenvolvendo um aplicativo de área de trabalho do Windows 8 ou um aplicativo de dispositivo de área de trabalho do Windows 8, poderá instalar e executar o Windows 8 ou Windows 8.1.
-   Se você estiver desenvolvendo um aplicativo de área de trabalho Windows 8.1 ou aplicativo de dispositivo de área de trabalho do Windows 8, instale Windows 8.1.

2. Instale o [Kit de certificação de aplicativos do windows 3,3](/previous-versions//mt637081(v=vs.85)), que está incluído no SDK (Software Development Kit) do windows para Windows 8.1.

**Observação:** Ao instalar o kit de certificação de aplicativos do Windows 3,3 ou superior em seu computador, você substitui qualquer versão do kit instalada anteriormente.

## <a name="instructions-to-run-windows-app-certification-kit-33"></a>Instruções para executar o kit de certificação de aplicativos para Windows 3,3

**Valide seu aplicativo de desktop usando o kit de certificação de aplicativos do Windows 3,3 interativamente**

1.  No menu Iniciar, pesquise por kit de certificado de aplicativo do Windows.
2.  No kit de certificação de aplicativos do Windows, clique na categoria validação de teste que você deseja executar. Se você estiver validando um aplicativo de área de trabalho, selecione **validar aplicativo de área de trabalho**.
3.  Na próxima tela, navegue até o arquivo de instalação do aplicativo de desktop que você deseja validar.
    -   **Observação:** Você pode usar as [etapas da linha de comando](#commandlinesteps) para incluir opções ou uma opção de instalação, se necessário.
4.  Indique o tipo de uso do aplicativo e clique em **Avançar**. O kit de certificação de aplicativos para Windows inicia a instalação do aplicativo de desktop usando os arquivos de instalação para que ele possa validar a instalação.
5.  Se for solicitado que você reinicialize o sistema para concluir a instalação, escolha **não**. Se seu aplicativo precisar instalar vários componentes ou dependências externas, selecione cuidadosamente o nome do seu aplicativo. O nome escolhido aqui é o nome que seu aplicativo recebe se ele for listado na Windows Store. Quando a validação for concluída, salve o relatório com o nome que você deu a seu aplicativo na etapa 6. O kit de certificação de aplicativos para Windows cria um arquivo de relatório XML e o salva.
6.  Navegue até a pasta em que você salvou o relatório e abra-o para exibir os resultados do teste. Se o teste falhou e você está qualificado para uma renúncia, as informações que você precisa enviar estão listadas aqui. Você deve enviar uma descrição detalhada para cada solicitação de renúncia possível.

**Validar seu aplicativo de área de trabalho do Windows usando o kit de certificação de aplicativos do Windows 3,3 de uma linha de comando**

1.  Navegue até a pasta em que você salvou o relatório e abra-o para exibir os resultados do teste. Os testes com falha com uma possível solicitação de renúncia estão listados aqui. Você deve enviar uma descrição detalhada para cada solicitação de renúncia possível.
2.  Na pasta que contém o kit de certificação de aplicativos do Windows, insira estes comandos nesta ordem:

    -   <span id="commandLineSteps"></span><span id="commandlinesteps"></span><span id="COMMANDLINESTEPS"></span>`appcert.exe reset`
    -   `appcert test -apptype desktop -setuppath d:\cdrom\setup.exe  -appusage peruser -reportoutputpath [report file name]`

    Onde: `[report file name]` é o nome de arquivo totalmente qualificado do arquivo XML que o kit criará para conter o relatório de teste.

3.  Após a conclusão do teste, abra o arquivo de relatório chamado \[ nome \] do arquivo de relatório e exiba os resultados do teste.

    **Observação:** Para obter mais informações sobre a linha de comando do kit de certificação de aplicativos do Windows, digite o comando appcert.exe/?

    O kit de certificação de aplicativos para Windows deve ser executado no contexto de uma sessão de usuário ativa, mas você não pode iniciar aplicativos em uma sessão não interativa. A maneira como o kit manipula tokens para executar testes com ou sem privilégios administrativos depende também desse contexto de sessão de usuário. O kit pode ser executado de um serviço, mas o serviço deve ser capaz de gerar o processo do kit em uma sessão de usuário ativa.

**Use o kit de certificação de aplicativos do Windows para validar seus aplicativos do Windows 7**

-   O kit de certificação de aplicativos para Windows substituiu o kit de logotipo de software do Windows. Se você quiser o logotipo do Windows 7 para seu aplicativo, use o kit de certificação de aplicativos do Windows para seu relatório e teste de validação. O kit pode detectar em qual sistema operacional ele está sendo executado e é iniciado automaticamente para aplicativos do Windows 7. Siga o mesmo processo para validar os aplicativos do Windows 7.

**Enviar para certificação**

-   Depois que seu aplicativo for validado, você estará pronto para enviá-lo para [a certificação por meio do processo de envio do portal](https://www.microsoft.com/?ref=go).

## <a name="reference-documents"></a>Documentos de referência

-   [Requisitos de certificação para aplicativos da área de trabalho do Windows](/windows/desktop/win_cert/certification-requirements-for-windows-desktop-apps)
-   [white paper de certificação de aplicativo](https://www.microsoft.com/download/details.aspx?id=27414)
-   [Integração da Windows Store para aplicativos da área de trabalho](/previous-versions//dn322034(v=vs.85))
-   [Requisitos de certificação de aplicativos para desktop do Windows 7](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)

## <a name="windows-app-certification-kit-tests"></a>Testes do Kit de Certificação de Aplicativos Windows

Alteramos o kit para facilitar o uso dos [testes de ACK do Windows](windows-app-certification-kit-tests.md) . O kit agora tem:

-   Uma nova interface do usuário simplificada
-   Teste de vários usuários aprimorado, que não exige mais que você configure uma segunda conta de usuário

 

 