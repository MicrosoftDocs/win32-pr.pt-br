---
title: Sobre URLs SAMI
description: Sobre URLs SAMI
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Windows Media Player, SAMI (intercâmbio de mídia acessível) sincronizado
- modelo de objeto Windows Media Player, SAMI (intercâmbio de mídia acessível) sincronizado
- modelo de objeto, SAMI (intercâmbio de mídia acessível) sincronizado
- Windows Media Player SAMI (intercâmbio de mídia acessível) móvel, sincronizado
- Windows Media Player controle de ActiveX, SAMI (intercâmbio de mídia acessível) sincronizado
- Windows Media Player controle de ActiveX móvel, SAMI (sincronização de mídia acessível)
- ActiveX controle, SAMI (intercâmbio de mídia acessível) sincronizado
- Arquivos SAMI (intercâmbio de mídia acessível) sincronizados
- SAMI (sincronizado com o intercâmbio de mídia acessível), arquivos
- SAMI (sincronização de mídia acessível), URLs
- SAMI (sincronizado com o intercâmbio de mídia acessível), URLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a35976c6988ad4298c812005002da010730d5254bd7c010f24fe32741be393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956796"
---
# <a name="about-sami-urls"></a>Sobre URLs SAMI

Os arquivos SAMI podem ser associados a arquivos de mídia digital usando uma única URL. Isso é feito usando *o parâmetro de URL Sami* . O parâmetro de URL é precedido pela URL base e um? . Uma URL com um parâmetro *Sami* segue esta sintaxe:

*URL*? *Sami* = *captionsURL*.

O valor do parâmetro URL segue o nome do parâmetro e um sinal de igual, como no exemplo a seguir:


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



essa sintaxe de URL é comumente usada em um hiperlink ou em um Windows metarquivo de mídia para vincular diretamente aos locais do arquivo de mídia digital e do arquivo SAMI. quando o usuário clica no hiperlink, Windows Media Player é iniciado no modo completo e reproduz o conteúdo de mídia digital.

se o parâmetro de URL *sami* não for especificado, Windows Media Player procurará um arquivo sami que esteja no mesmo local que o arquivo de mídia digital e que tenha o mesmo nome de arquivo, exceto para a extensão de nome de arquivo, que deve ser. smi. Se esse arquivo estiver presente, ele será aberto automaticamente se a exibição da legenda tiver sido habilitada no Player.

as legendas ocultas são habilitadas no Windows Media Player clicando no menu **reproduzir** , clicando em **legendas e legendas** e clicando **em**. Se as legendas ocultas estiverem habilitadas, as legendas contidas no arquivo SAMI serão exibidas enquanto o item de mídia for reproduzido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




