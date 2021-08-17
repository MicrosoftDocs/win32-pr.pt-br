---
title: Exemplo da Galeria
description: Este exemplo de código demonstra a marcação e o código necessários para usar os diferentes tipos de controles da Galeria incluídos na estrutura Windows Faixa de Opções.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 8c62e8955e737ac78ee5543c0a12febc5436bacd7f9d739bc9af02bacd555d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706702"
---
# <a name="gallery-sample"></a>Exemplo da Galeria

Este exemplo de código demonstra a marcação e o código necessários para usar os diferentes tipos de controles da Galeria incluídos na estrutura Windows Faixa de Opções. O exemplo inclui código que pode ser usado para popular dinamicamente itens nas Galerias e manipular eventos especiais de visualização da Galeria que suportam a interface do usuário orientada a resultados.

- [Usage](#usage)
  - [Compilando o exemplo](#building-the-sample)
  - [Executando o exemplo](#running-the-sample)
- [Suporte](#support)
- [Requisitos mínimos](#minimum-requirements)
- [Tópicos relacionados](#related-topics)

## <a name="usage"></a>Uso

Os exemplos da estrutura Windows Ribbon podem ser baixados como projetos Microsoft Visual Studio autônomos do Centro de Download da [Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) ou instalados como parte do [SDK (Software Development Kit)](https://developer.microsoft.com/windows/downloads/sdk-archive/)do Windows.

- Windows Software Development Kit (SDK) (caminho de instalação padrão): %ProgramFiles% SDKs da Microsoft Windows número de versão \\ \\ \\ \[ \] \\ Exemplos \\ winui \\ WindowsRibbon \\ Gallery

### <a name="building-the-sample"></a>Compilando o exemplo

Baixe o exemplo.

Instale o Windows SDK do Windows 7 e abra sua janela de comando do ambiente de build. No menu Iniciar, aponte para Todos os Programas, Microsoft Windows SDK e clique em CMD Shell.

Para compilar o exemplo da janela de comando do ambiente de compilação, vá para o diretório fonte do exemplo. No prompt de comando, digite MSBUILD.

Para compilar o exemplo no Microsoft Visual Studio, carregue a solução or arquivo do projeto do exemplo e então pressione CTRL+SHIFT+B.

### <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo na janela de comando do ambiente de build, execute os arquivos .exe na pasta Bin Debug ou Bin Release contida na pasta de origem \\ \\ de exemplo.

Para executar o exemplo compilado com a depuração no Visual Studio, pressione F5.

## <a name="support"></a>Suporte

O [Fórum Windows de Desenvolvimento](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) da Faixa de Opções está disponível para discutir tópicos e fazer perguntas relacionadas ao desenvolvimento de aplicativos Windows Faixa de Opções.

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

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com galerias](ribbon-controls-galleries.md)
</dt> <dt>

[Caixa de combinação](windowsribbon-controls-combobox.md)
</dt> <dt>

[Galeria de lista listada](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[Galeria na Faixa de Opções](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Galeria de Botões divididos](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Propriedades da coleção](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





