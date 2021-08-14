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
- registro, configurações para Windows Media Player
- configurações do registro de extensão de nome de arquivo
- biblioteca, entradas do registro de classificação
- biblioteca, registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cb263732dc8071d603c5acd62db25fc8ee887c35b28d109d961a63aba80d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575126"
---
# <a name="library-classification-registry-entries"></a>Entradas do registro de classificação de biblioteca

quando Windows Media Player encontra um arquivo de mídia que tem uma extensão de nome de arquivo personalizada, ele não sabe se o arquivo deve ser classificado como áudio, vídeo ou algum outro tipo. por padrão, Windows Media Player coloca esses arquivos na parte de outra mídia da biblioteca.

se os arquivos de mídia digital tiverem um formato personalizado, você poderá fornecer Windows Media Player com informações sobre onde os arquivos devem aparecer na biblioteca do Player, colocando duas entradas no registro no computador do usuário.

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

[**Configurações de registro de extensão de nome de arquivo**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




