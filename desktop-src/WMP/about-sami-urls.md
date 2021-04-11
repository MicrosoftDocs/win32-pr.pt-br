---
title: Sobre URLs SAMI
description: Sobre URLs SAMI
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Windows Media Player, SAMI (intercâmbio de mídia acessível) sincronizado
- Modelo de objeto do Windows Media Player, SAMI (sincronização de mídia acessível)
- modelo de objeto, SAMI (intercâmbio de mídia acessível) sincronizado
- Windows Media Player Mobile, SAMI (sincronização de mídia acessível) sincronizado
- Controle ActiveX do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX móvel do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX, SAMI (sincronização de mídia acessível)
- Arquivos SAMI (intercâmbio de mídia acessível) sincronizados
- SAMI (sincronizado com o intercâmbio de mídia acessível), arquivos
- SAMI (sincronização de mídia acessível), URLs
- SAMI (sincronizado com o intercâmbio de mídia acessível), URLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a41e70d0239b9bdac7d12f9a2dd2f75be15b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159629"
---
# <a name="about-sami-urls"></a>Sobre URLs SAMI

Os arquivos SAMI podem ser associados a arquivos de mídia digital usando uma única URL. Isso é feito usando *o parâmetro de URL Sami* . O parâmetro de URL é precedido pela URL base e um? . Uma URL com um parâmetro *Sami* segue esta sintaxe:

*URL*? *Sami* = *captionsURL*.

O valor do parâmetro URL segue o nome do parâmetro e um sinal de igual, como no exemplo a seguir:


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



Essa sintaxe de URL é comumente usada em um hiperlink ou um metarquivo do Windows Media para vincular diretamente os locais do arquivo de mídia digital e do arquivo SAMI. Quando o usuário clica no hiperlink, o Windows Media Player é iniciado no modo completo e reproduz o conteúdo de mídia digital.

Se o parâmetro de URL *Sami* não for especificado, o Windows Media Player procurará um arquivo Sami que esteja no mesmo local que o arquivo de mídia digital e que tenha o mesmo nome de arquivo, exceto para a extensão de nome de arquivo, que deve ser. SMI. Se esse arquivo estiver presente, ele será aberto automaticamente se a exibição da legenda tiver sido habilitada no Player.

As legendas ocultas são habilitadas no Windows Media Player clicando no menu **reproduzir** , clicando em **legendas e legendas** e, em seguida, clicando **em**. Se as legendas ocultas estiverem habilitadas, as legendas contidas no arquivo SAMI serão exibidas enquanto o item de mídia for reproduzido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




