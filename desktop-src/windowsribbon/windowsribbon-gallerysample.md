---
title: Exemplo de galeria
description: Este exemplo de código demonstra a marcação e o código necessários para usar os diferentes tipos de controles da Galeria incluídos na estrutura da faixa de tipos do Windows.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aacc52081fbcd2b6b58fd4c2439894705880d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085294"
---
# <a name="gallery-sample"></a>Exemplo de galeria

Este exemplo de código demonstra a marcação e o código necessários para usar os diferentes tipos de controles da Galeria incluídos na estrutura da faixa de tipos do Windows. O exemplo inclui código que pode ser usado para popular dinamicamente os itens nas galerias e manipular eventos de visualização de galeria especiais que dão suporte à interface do usuário orientada por resultados.

-   [Usage](#usage)
    -   [Compilando o exemplo](#building-the-sample)
    -   [Executando o exemplo](#running-the-sample)
-   [Suporte](#support)
-   [Requisitos mínimos](#minimum-requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="usage"></a>Uso

O exemplo de galeria pode ser baixado como um projeto de Microsoft Visual Studio autônomo do [centro de download da Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) ou instalado como parte do [SDK (Software Development Kit) do Windows](https://msdn.microsoft.com/windows/bb980924.aspx).

-   Centro de download da Microsoft: [exemplos de faixa](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en) de medida do Windows
-   SDK (Software Development Kit) do Windows (caminho de instalação padrão):% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ número de versão \] \\ amostras \\ WinUI \\ WindowsRibbon \\ Gallery

### <a name="building-the-sample"></a>Compilando o exemplo

Baixe o exemplo no seu disco rígido.

Instale o SDK do Windows para o Windows 7 e abra sua janela de comando de ambiente de compilação. No menu Iniciar, aponte para Todos os Programas, Microsoft Windows SDK e clique em CMD Shell.

Para compilar o exemplo da janela de comando do ambiente de compilação, vá para o diretório fonte do exemplo. No prompt de comando, digite MSBUILD.

Para compilar o exemplo no Microsoft Visual Studio, carregue a solução or arquivo do projeto do exemplo e então pressione CTRL+SHIFT+B.

### <a name="running-the-sample"></a>Executando o exemplo

Para executar o exemplo na janela de comando compilar ambiente, execute os arquivos. exe na pasta de \\ depuração bin ou \\ solte contida na pasta de origem de exemplo.

Para executar o exemplo compilado com a depuração no Visual Studio, pressione F5.

## <a name="support"></a>Suporte

O [Fórum de desenvolvimento da faixa](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de Dasgem do Windows está disponível para discutir tópicos e fazer perguntas relacionadas ao desenvolvimento de aplicativos da faixa de de uma Windows.

## <a name="minimum-requirements"></a>Requisitos mínimos



| Requisito | Valor |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 7<br/> Windows Vista com Service Pack 2 (SP2) e [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Servidor mínimo com suporte | Windows Server 2008 R2<br/> Windows Server 2008 com SP2 e [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| SDK do Windows              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Cabeçalhos e arquivos IDL     | uiribbon. h, uiribbon. idl                                                                                                                                                 |



 

> [!Note]  
> A [atualização de plataforma para o Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e [a atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) são conjuntos de bibliotecas de tempo de execução que permitem aos desenvolvedores direcionar aplicativos de faixa de opções do Windows para o Windows Vista e o Windows Server 2008. As atualizações de plataforma estarão disponíveis para todos os clientes do Windows Vista e do Windows Server 2008 por meio do Windows Update. Aplicativos de terceiros que exigem [atualização de plataforma para Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou [atualização de plataforma para Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) podem ter Windows Update detectar se a atualização necessária está instalada; Se não estiver, Windows Update será baixado e instalado em segundo plano.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com galerias](ribbon-controls-galleries.md)
</dt> <dt>

[Caixa de combinação](windowsribbon-controls-combobox.md)
</dt> <dt>

[Galeria suspensa](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[Galeria de faixa de bits](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Propriedades da coleção](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





