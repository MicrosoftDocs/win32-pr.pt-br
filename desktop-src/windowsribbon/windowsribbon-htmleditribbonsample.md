---
title: Exemplo de HTMLEditRibbon
description: Este exemplo de código mostra a marcação e o código necessários para migrar um aplicativo MFC (MFC) existente para usar a Faixa Windows Faixa de Opções.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 0f1299bdc20b1b94a5113d3cfcdda205b6ad8e513a59706d708362fbc8383bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202113"
---
# <a name="htmleditribbon-sample"></a>Exemplo de HTMLEditRibbon

Este exemplo de código mostra a marcação e o código necessários para migrar um aplicativo MFC (MFC) existente para usar a Faixa Windows Faixa de Opções. Ele foi criado por meio do aplicativo de exemplo HTMLEdit MFC existente e modificando seu código e recursos para usar a faixa de opções Windows aplicativo.

- [Comentários](#remarks)
- [Usage](#usage)
  - [Compilando o exemplo](#building-the-sample)
  - [Executando o exemplo](#running-the-sample)
- [Suporte](#support)
- [Requisitos mínimos](#minimum-requirements)

## <a name="remarks"></a>Comentários

Para o exemplo de MFC, consulte [HtmlEdit Sample: Wraps the Internet Explorer MSHTML Editing Control](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).

## <a name="usage"></a>Uso

Os exemplos da estrutura Windows Ribbon podem ser baixados como projetos Microsoft Visual Studio autônomos do Centro de Download da [Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) ou instalados como parte do [SDK (Software Development Kit)](https://developer.microsoft.com/windows/downloads/sdk-archive/)do Windows.

- Windows Software Development Kit (SDK) (caminho de instalação padrão): %ProgramFiles% SDKs da Microsoft Windows número de versão \\ \\ \\ \[ \] \\ Exemplos \\ winui \\ WindowsRibbon \\ HTMLEditRibbon

### <a name="building-the-sample"></a>Compilando o exemplo

Baixe o exemplo.

Instale o Windows SDK do Windows 7 e abra sua janela de comando do ambiente de build. No menu Iniciar, aponte para Todos os Programas, Microsoft Windows SDK e clique em CMD Shell.

Para compilar o exemplo da janela de comando do ambiente de compilação, vá para o diretório fonte do exemplo. No prompt de comando, digite MSBUILD.

Para compilar o exemplo no Microsoft Visual Studio, carregue a solução or arquivo do projeto do exemplo e então pressione CTRL+SHIFT+B.

### <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo na janela de comando do ambiente de build, execute os arquivos .exe na pasta Bin Debug ou Bin Release contida na pasta de origem \\ \\ de exemplo.

Para executar o exemplo compilado com a depuração no Visual Studio, pressione F5.

## <a name="support"></a>Suporte

O [Fórum Windows Desenvolvimento](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) da Faixa de Opções do Windows está disponível para discutir tópicos e fazer perguntas relacionadas ao desenvolvimento de aplicativos Windows Faixa de Opções.

## <a name="minimum-requirements"></a>Requisitos mínimos



| Requisito | Valor |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 7<br/> Windows Vista com Service Pack 2 (SP2) e [Atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Servidor mínimo com suporte | Windows Server 2008 R2<br/> Windows Server 2008 com SP2 e [Atualização de Plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| SDK do Windows              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Arquivos de IDL e de header     | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> A Atualização de Plataforma para [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e Atualização de Plataforma para o Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) são conjuntos de bibliotecas em tempo de run time que permitem aos desenvolvedores direcionar aplicativos da Faixa de Opções do Windows para o Windows Vista e o Windows Server 2008. As atualizações da plataforma estarão disponíveis para todos os clientes Windows Vista e Windows Server 2008 por meio do Windows Update. Aplicativos de terceiros que exigem a Atualização de Plataforma para Windows Vista ou Atualização de Plataforma para [o Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) podem fazer com que Windows Atualização detecte se [a](https://msdn.microsoft.com/library/dd378748.aspx) atualização necessária está instalada; se não estiver, Windows Update baixará e o instalará em segundo plano.

 

 

 





