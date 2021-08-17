---
title: Registro de monitoramento de pastas Configurações
description: Registro de monitoramento de pastas Configurações
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Windows Media Player,configurações do Registro de monitoramento de pasta
- Windows Media Player, configurações do Registro de monitoramento de pasta de arquivos
- Windows Media Player,Registro
- registro, configurações de monitoramento de pasta
- registro, configurações de monitoramento de pasta de arquivos
- registry,settings for Windows Media Player
- configurações do Registro de monitoramento de pasta
- configurações do Registro de monitoramento de pasta de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3e5e99c633c58a68b3579c55d38e6ad5b2415d9faac8d6c3438251c5a83459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748437"
---
# <a name="folder-monitoring-registry-settings"></a>Registro de monitoramento de pastas Configurações

Windows Media Player série 9 ou posterior pode monitorar pastas de arquivos para novos arquivos de mídia digital. Quando o Player detecta um novo arquivo em uma pasta monitorada, ele adiciona automaticamente o arquivo à biblioteca. Por Windows Media Player 9 a Windows Media Player 11, os usuários podem alterar a lista  de pastas monitoradas clicando  em Monitorar Pastas na guia biblioteca da caixa de diálogo Opções. Por Windows Media Player 12, um usuário pode alterar a lista de pastas monitoradas seguindo as instruções no tópico Adicionar itens à [biblioteca Windows Media Player .](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library) Por Windows Media Player de 9 a Windows Media Player 11, você pode adicionar programaticamente uma pasta a ser monitorada adicionando um valor ao Registro. Por Windows Media Player 12, não é possível usar o Registro para adicionar ou remover pastas a serem monitoradas programaticamente.

Para Windows Media Player de 9 a Windows Media Player 11, para adicionar uma pasta para monitoramento, você deve primeiro criar ou modificar dois valores na seguinte chave do Registro:

**Preferências do Microsoft \_ \_ \\ MediaPlayer do software \\ \\ de usuário atual \\ do HKEY\\**

Os novos valores devem ser nomeados da seguinte forma.



| Nome                           | Tipo           | Descrição                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TrackFoldersDirectories**    | **REG \_ DWORD** | Um **valor DWORD** que representa a contagem de pastas a monitorar. Isso deve corresponder à contagem de **valores TrackFoldersDirectories**_X._                                                                                                                                         |
| **TrackFoldersDirectories**_X_ | **REG \_ SZ**    | Um valor de cadeia de caracteres que representa o caminho da pasta a ser monitorada. Cada pasta a ser monitorada requer um valor separado. O sufixo *X* é um inteiro que sempre deve começar em 0 e, em seguida, incrementar em 1. Windows Media Player também monitora subpastas da pasta especificada. |



 

Por exemplo, para adicionar a primeira pasta a ser monitorada, adicione o seguinte valor:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



Em seguida, crie o valor de contagem:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



Para adicionar uma segunda pasta a ser monitorada, adicione o seguinte valor:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



Em seguida, incremente o valor de contagem:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do Registro**](registry-settings.md)
</dt> </dl>

 

 




