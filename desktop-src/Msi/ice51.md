---
description: ICE51 verifica se um título foi fornecido para arquivos de recurso de fonte.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170841"
---
# <a name="ice51"></a>ICE51

ICE51 verifica se um título foi fornecido para arquivos de recurso de fonte.

Você deve fornecer um título para um recurso de fonte que não tenha um nome inserido. Somente os arquivos de recurso de fonte. TTC,. ttf e. otf não exigem um título, pois esses arquivos contêm um nome inserido. Não forneça um título para um recurso de fonte que contenha um nome inserido porque o sistema registra a fonte duas vezes.

**[Windows Installer 4,5 e anteriores](not-supported-in-windows-installer-4-5.md):** ICE51 não verifica os arquivos de recurso de fonte. otf.

## <a name="result"></a>Resultado

ICE51 posta um erro se houver algum arquivo de recurso de fonte. TTC,. ttf e. otf com títulos. ICE51 posta um aviso se houver outros arquivos de recurso de fonte sem título.

## <a name="example"></a>Exemplo

ICE51 relataria o seguinte aviso para o exemplo mostrado.

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

ICE51 relataria a seguinte mensagem de erro para o exemplo mostrado.

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | FileName  |
|-------|-----------|
| Font1 | font1. ttf |
| Font2 | font2. Fon |



 

[Tabela de fontes](font-table.md)



| Arquivo\_ | FontTitle          |
|--------|--------------------|
| Font1  | Uma fonte realmente interessante |
| Font2  |                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



