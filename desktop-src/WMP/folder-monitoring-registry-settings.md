---
title: Configurações do registro de monitoramento de pasta
description: Configurações do registro de monitoramento de pasta
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Windows Media Player, configurações do registro de monitoramento de pasta
- Windows Media Player, configurações do registro de monitoramento de pasta de arquivos
- Windows Media Player, registro
- registro, configurações de monitoramento de pasta
- registro, configurações de monitoramento de pasta de arquivo
- registro, configurações do Windows Media Player
- configurações do registro de monitoramento de pasta
- configurações do registro de monitoramento da pasta de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233076d1fc807dd5cdd79e9b4985ef752fba0815
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366826"
---
# <a name="folder-monitoring-registry-settings"></a>Configurações do registro de monitoramento de pasta

O Windows Media Player 9 Series ou posterior pode monitorar pastas de arquivos para novos arquivos de mídia digital. Quando o Player detecta um novo arquivo em uma pasta monitorada, ele adiciona automaticamente o arquivo à biblioteca. Para o Windows Media Player 9 até o Windows Media Player 11, os usuários podem alterar a lista de pastas monitoradas clicando em **monitorar pastas** na guia Biblioteca da caixa de diálogo **Opções** . Para o Windows Media Player 12, um usuário pode alterar a lista de pastas monitoradas seguindo as instruções no tópico [Adicionar itens à biblioteca do Windows Media Player](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library). Para o Windows Media Player 9 até o Windows Media Player 11, você pode adicionar programaticamente uma pasta a ser monitorada, adicionando um valor ao registro. Para o Windows Media Player 12, você não pode usar o registro para adicionar ou remover programaticamente pastas a serem monitoradas.

Para o Windows Media Player 9 até o Windows Media Player 11, para adicionar uma pasta para monitoramento, você deve primeiro criar ou modificar dois valores na seguinte chave do registro:

**HKEY \_ Current \_ user \\ software \\ usuário \\ preferências do Microsoft MediaPlayer \\\\**

Os novos valores devem ser nomeados da seguinte maneira.



| Nome                           | Tipo           | Descrição                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TrackFoldersDirectories**    | **REG \_ DWORD** | Um valor **DWORD** que representa a contagem de pastas a serem monitoradas. Isso deve corresponder à contagem de **TrackFoldersDirectories * * * X* valores.                                                                                                                                         |
| **TrackFoldersDirectories * * * X* | **REG \_ sz**    | Um valor de cadeia de caracteres que representa o caminho da pasta a ser monitorada. Cada pasta a ser monitorada requer um valor separado. O sufixo *X* é um inteiro que sempre deve começar em 0 e, em seguida, incrementado em 1. O Windows Media Player também monitora as subpastas da pasta especificada. |



 

Por exemplo, para adicionar a primeira pasta a ser monitorada, adicione o seguinte valor:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



Em seguida, crie o valor da contagem:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



Para adicionar uma segunda pasta a ser monitorada, adicione o seguinte valor:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



Em seguida, aumente o valor da contagem:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do registro**](registry-settings.md)
</dt> </dl>

 

 




