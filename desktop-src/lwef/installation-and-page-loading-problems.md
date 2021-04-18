---
title: Problemas de instalação e carregamento de página
description: Problemas de instalação e carregamento de página
ms.assetid: 1611c3f1-0411-4631-a64c-e7637fc7edd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9775e6a9afa957867d5279b9faaf506e32757f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "105788089"
---
# <a name="installation-and-page-loading-problems"></a>Problemas de instalação e carregamento de página

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

### <a name="when-i-attempt-to-install-microsoft-agent-on-microsoft-windows-nt-i-get-a-message-indicating-that-i-need-to-be-an-administrator"></a>Quando tento instalar o Microsoft Agent no Microsoft Windows NT, recebo uma mensagem indicando que preciso ser um administrador.

Como o Microsoft Agent grava arquivos no diretório do sistema quando ele é instalado, você deve ter privilégios de administrador (não de usuário) para instalar o.

### <a name="when-i-attempt-to-install-microsoft-agent-i-get-one-of-the-following-errors-process-regsvr32-s-windowsmsagentagentctldll-error-while-creating-this-file-cannot-find-this-file-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows-a-required-dll-msvcrtdll-was-not-found-error-creating-process-cwindowsmsagentagentsvrexe-regserver-reason-one-of-the-library-files-needed-to-run-this-application-cannot-be-found-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows"></a>Quando tento instalar o Microsoft Agent, obtenho um dos seguintes erros: Process (regsvr32/s Windows \\ msagent \\AgentCtl.dll). Erro ao criar este arquivo. Não é possível localizar este arquivo. (Observação: o local do diretório citado na mensagem de erro varia dependendo de como você instalou o Windows.) Um MSVCRT.DLL DLL necessário não foi encontrado. Erro ao criar o processo <c: \\ Windows \\ MSAgent \\agentsvr.exe/RegServer>. Motivo: um dos arquivos de biblioteca necessários para executar este aplicativo não pode ser encontrado. (Observação: o local do diretório citado na mensagem de erro varia dependendo de como você instalou o Windows.)

A instalação do Microsoft Agent requer a instalação correta do Regsvr32.exe, Msvcrt.dll (biblioteca de tempo de execução do Microsoft C) e DLLs OLE atualizadas. Consulte Atualização do DCOM: ( <https://docs.microsoft.com/openspecs/windows_protocols/ms-dcom/4a893f3d-bd29-48cd-9f43-d9777a4415b0> ). A melhor maneira de garantir que todos os arquivos de sistema corretos estejam presentes é instalar o [Microsoft Internet Explorer 4,0](https://www.microsoft.com/ie/download) ou posterior.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-a-scripting-error-vbscript-runtime-error-object-required"></a>Quando tento carregar uma página com script para o Microsoft Agent, obtenho um erro de script: "erro de tempo de execução VBScript, objeto necessário."

Uma das condições a seguir pode fazer com que a mensagem seja exibida:

-   As opções de segurança do Microsoft Internet Explorer devem ser definidas para habilitar os controles e plug-ins do ActiveX. Verifique a página de segurança do navegador. No Microsoft Internet Explorer, abra o menu Exibir, escolha opções, clique na guia Segurança e verifique se a caixa de seleção Habilitar controles ActiveX e Plug-Ins está marcada.
-   Você está executando em um sistema Windows 9x ou Windows NT de inicialização dupla e instalou o Microsoft Agent em um sistema operacional, mas está tentando acessar a página do outro sistema operacional. Embora os sistemas operacionais possam compartilhar diretórios e arquivos, as informações de registro usadas pelo Microsoft Agent não são compartilhadas, portanto, você deve instalar o Microsoft Agent no sistema operacional usado para acessar as páginas da Web com o caractere em script.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-nothing-happens"></a>Quando tento carregar uma página com script para o Microsoft Agent, nada acontece.

Isso pode ocorrer se uma das seguintes condições existir:

-   Verifique as opções de segurança do navegador. Seu navegador deve ser definido para habilitar o carregamento de scripts ActiveX e a reprodução de controles ActiveX.
-   Se estiver acessando páginas com script com o Microsoft Agent e usando o Microsoft Internet Explorer, você deverá ter a versão 3, 2 ou posterior (Baixe a versão mais recente do Internet Explorer em [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) <https://www.microsoft.com/windows/ie/> ). No Microsoft Internet Explorer, abra o menu Exibir, escolha opções, clique na guia Segurança e marque todas as caixas de seleção de conteúdo ativo.
-   Um miniaplicativo Java na página também pode causar esse erro. Para executar o Microsoft Agent na mesma página que um miniaplicativo Java requer a versão 2,0 da máquina virtual (VM) da Microsoft. Para obter mais informações, consulte as [perguntas frequentes sobre programação/script](programming-scripting-faq.md).

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-unable-to-initialize-microsoft-agent"></a>Quando tento carregar uma página com script para o Microsoft Agent, recebo a mensagem "não é possível inicializar o Microsoft Agent".

Isso geralmente ocorre quando você não tem o Microsoft Agent ou algum outro controle que a página usa instalada e escolhe não quando for solicitado a instalar o controle. Tente atualizar a página, embora a página possa funcionar apenas se você instalar todos os componentes necessários.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-the-component-has-been-digitally-signed-by-its-publisher-but-the-signature-does-not-match-the-component-it-is-possible-that-this-component-has-been-damaged-or-tampered-with-do-you-want-to-continue"></a>Quando tento carregar uma página com script para o Microsoft Agent, recebo a mensagem "o componente foi digitalmente" assinado "por seu editor, mas a assinatura não corresponde ao componente. É possível que esse componente tenha sido danificado ou adulterado? Deseja continuar?"

Isso pode ser exibido se você tentar instalar o Microsoft Agent no Microsoft Internet Explorer 3, 2. Você pode continuar com a instalação ou atualizar seu navegador para o Internet Explorer 4,0 ou posterior.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-using-netscape-navigator-or-other-internet-browsers-i-get-errors"></a>Quando tento carregar uma página com script para o Microsoft Agent usando o Netscape Navigator (ou outros navegadores da Internet), recebo erros.

O Microsoft Agent é implementado usando interfaces ActiveX. Você pode usá-lo somente com um navegador (como o Microsoft Internet Explorer) que dá suporte à inserção de objetos ActiveX por meio de script em uma página e somente em sistemas que executam o Microsoft Windows 95, Windows 98 e Windows NT 4,0 (ou posterior). Se você não estiver usando o Microsoft Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ), consulte o fornecedor do seu navegador para obter mais informações sobre o suporte do ActiveX.

 

 




