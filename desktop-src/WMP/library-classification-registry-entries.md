---
title: Entradas do registro de classificação de biblioteca
description: Entradas do registro de classificação de biblioteca
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Windows Media Player, biblioteca
- Windows Media Player, entradas do registro de classificação
- Windows Media Player, extensões de nome de arquivo
- Windows Media Player, registro
- registro, extensões de nome de arquivo
- registro, entradas de classificação de biblioteca
- registro, configurações do Windows Media Player
- configurações do registro de extensão de nome de arquivo
- biblioteca, entradas do registro de classificação
- biblioteca, registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781425"
---
# <a name="library-classification-registry-entries"></a>Entradas do registro de classificação de biblioteca

Quando o Windows Media Player encontra um arquivo de mídia que tem uma extensão de nome de arquivo Personalizada, ele não sabe se o arquivo deve ser classificado como áudio, vídeo ou algum outro tipo. Por padrão, o Windows Media Player coloca esses arquivos na parte de outra mídia da biblioteca.

Se os arquivos de mídia digital tiverem um formato personalizado, você poderá fornecer ao Windows Media Player informações sobre onde os arquivos devem aparecer na biblioteca do Player, colocando duas entradas no registro no computador do usuário.

Uma entrada é exibida na subchave a seguir.

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MediaPlayer \\ MLS \\ extensões**

A entrada do registro tem o formato a seguir.



| Nome                                                  | Tipo de dados   | Valor                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| A extensão de nome de arquivo sem o separador de ponto (.) | **REG \_ sz** | Uma cadeia de caracteres que especifica um local de biblioteca |



 

A outra entrada do registro é exibida na subchave a seguir que você cria.

**HKEY \_ CustomExtension de classes \_ raiz \\** 

em que *customExtension* é a extensão de nome de arquivo, incluindo o separador de ponto (.).

A entrada do registro tem o formato a seguir.



| Nome          | Tipo de dados   | Valor                                      |
|---------------|-------------|--------------------------------------------|
| PerceivedType | **REG \_ sz** | Uma cadeia de caracteres que especifica um local de biblioteca |



 

Ambas as entradas do registro devem ter o mesmo valor. Os valores possíveis são fornecidos na tabela a seguir.



| Valor | Descrição                                                                      |
|-------|----------------------------------------------------------------------------------|
| áudio | Os arquivos que têm a extensão personalizada aparecem na parte de música da biblioteca. |
| video | Os arquivos que têm a extensão personalizada aparecem na parte de vídeo da biblioteca. |



 

Por exemplo, as seguintes entradas de registro especificam que os arquivos que têm a extensão de nome de arquivo. xyz aparecerão na parte de música da biblioteca:


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



Observe que qualquer código que tente gravar no registro no computador do usuário poderá gravar na \_ subárvore do computador local hKey \_ somente se o usuário atual tiver privilégios administrativos.

As entradas do registro de classificação de biblioteca têm suporte nas seguintes versões do Windows Media Player.

-   Windows Media Player 9 Series com hotfix 823275
-   Windows Media Player 10 e posterior

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do registro de extensão de nome de arquivo**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




