---
title: Exemplo de HTMLEditRibbon
description: este exemplo de código mostra a marcação e o código necessários para migrar um aplicativo de MFC (MFC) existente para usar a faixa de Windows.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: cfe75d13a69e0122766e51a00bcb1b15d52eab4e
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691705"
---
# <a name="htmleditribbon-sample"></a>Exemplo de HTMLEditRibbon

este exemplo de código mostra a marcação e o código necessários para migrar um aplicativo de MFC (MFC) existente para usar a faixa de Windows. ele foi criado por meio do aplicativo de exemplo MFC HTMLEdit existente e modificando seu código e recursos para usar a faixa de Windows.

- [Comentários](#remarks)
- [Usage](#usage)
  - [Compilando o exemplo](#building-the-sample)
  - [Executando o exemplo](#running-the-sample)
- [Suporte](#support)
- [Requisitos mínimos](#minimum-requirements)

## <a name="remarks"></a>Comentários

Para o exemplo de MFC, consulte [exemplo de HtmlEdit: encapsula o controle de edição MSHTML do Internet Explorer](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).

## <a name="usage"></a>Uso

os exemplos da estrutura da faixa de Microsoft Visual Studio Windows podem ser baixados como projetos autônomos do [centro de Download da Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) ou instalados como parte do [SDK (Software Development Kit) do Windows](https://developer.microsoft.com/windows/downloads/sdk-archive/).

- Windows SDK (Software Development Kit) (caminho de instalação padrão):% programfiles% \\ Microsoft SDKs \\ Windows \\ \[ número de versão \] \\ amostras \\ winui \\ WindowsRibbon \\ HTMLEditRibbon

### <a name="building-the-sample"></a>Compilando o exemplo

Baixe o exemplo.

instale o SDK do Windows para Windows 7 e abra sua janela de comando de ambiente de compilação. No menu Iniciar, aponte para Todos os Programas, Microsoft Windows SDK e clique em CMD Shell.

Para compilar o exemplo da janela de comando do ambiente de compilação, vá para o diretório fonte do exemplo. No prompt de comando, digite MSBUILD.

Para compilar o exemplo no Microsoft Visual Studio, carregue a solução or arquivo do projeto do exemplo e então pressione CTRL+SHIFT+B.

### <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo na janela de comando compilar ambiente, execute o .exe arquivos na pasta de \\ depuração bin ou \\ Release bin contida na pasta de origem de exemplo.

Para executar o exemplo compilado com a depuração no Visual Studio, pressione F5.

## <a name="support"></a>Suporte

o [fórum de desenvolvimento da faixa de Windows da Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) está disponível para discutir tópicos e fazer perguntas relacionadas ao desenvolvimento de aplicativos da faixa de.

## <a name="minimum-requirements"></a>Requisitos mínimos



| Requisito | Valor |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 7<br/> Windows vista com Service Pack 2 (SP2) e [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Servidor mínimo com suporte | Windows Server 2008 R2<br/> Windows servidor 2008 com SP2 e [atualização de plataforma para o Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| SDK do Windows              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Cabeçalhos e arquivos IDL     | uiribbon. h, uiribbon. idl                                                                                                                                                 |



 

> [!Note]  
> a [atualização de plataforma para o Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e [a atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) são conjuntos de bibliotecas de tempo de execução que permitem aos desenvolvedores direcionar Windows aplicativos de faixa de opções para o Windows Vista e o Windows Server 2008. as atualizações de plataforma estarão disponíveis para todos os clientes Windows Vista e Windows Server 2008 por meio do Windows Update. aplicativos de terceiros que exigem [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) podem ter Windows Update detectar se a atualização necessária está instalada; se não estiver, Windows Update será baixado e instalado em segundo plano.

 

 

 





