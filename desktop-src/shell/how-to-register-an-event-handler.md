---
description: Um dispositivo pode potencialmente gerar muitos eventos e cada evento tem a opção de ser manipulado por um de vários manipuladores diferentes.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Como registrar um manipulador de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f96aedc8b6b7944238938539a8fafa5d80c6dc7f1afd4dc5f818ecc91abd08c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090556"
---
# <a name="how-to-register-an-event-handler"></a>Como registrar um manipulador de eventos

Um dispositivo pode potencialmente gerar muitos eventos e cada evento tem a opção de ser manipulado por um de vários manipuladores diferentes. No Windows XP, os seguintes eventos são definidos:

-   DeviceArrival
-   DeviceRemoval
-   MediaArrival
-   MediaRemoval

## <a name="instructions"></a>Instruções


Os manipuladores de eventos são definidos na **chave EventHandlers.** Os valores de uma chave do manipulador de eventos são os nomes de cada manipulador que o usuário deve escolher quando o evento é detectado. Não há nenhum valor de dados associado a essas entradas. Veja a seguir uma definição de exemplo para um manipulador de eventos personalizado chamado **MyNewRemovalEventHandler**, que apresenta essas possibilidades de manipulador para o usuário:

-   Um manipulador a ser usado se o evento for detectado em um dispositivo feito pela empresa chamada Contoso, Inc.
-   Um manipulador a ser usado se o evento for detectado em um dispositivo feito pela empresa chamada Fabrikam, Inc.
-   Um manipulador a ser usado em todos os outros casos.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

Depois que um manipulador de eventos é definido, ele deve ser registrado com um manipulador de dispositivo para uma das possibilidades de evento: DeviceArrival, DeviceRemoval, MediaArrival ou MediaRemoval. MyNewRemovalEventHandler, definido anteriormente, é usado para DeviceRemoval em um manipulador de dispositivo personalizado chamado MyDeviceHandler e é definido para essa finalidade no exemplo a seguir. Novamente, o valor do Registro não tem nenhum componente de dados.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

Windows XP predefine o seguinte conjunto de EventHandlers. 

| Chave EventHandlers        | Tipo de mídia ou arquivo                             |
|--------------------------|------------------------------------------------|
| HandleCDBurningOnArrival | CD-R/CD-RW em branco                               |
| ShowPicturesOnArrival    | Arquivos de imagem                                  |
| PlayMusicFilesOnArrival  | Arquivos de música                                    |
| PlayVideoFilesOnArrival  | Arquivos de vídeo                                    |
| PlayCDAudioOnArrival     | CD de áudio (CD de formato REDBOOK com faixas de áudio) |
| PlayDVDMovieOnArrival    | Filmes de DVD                                     |



 

Windows O Vista predefine o seguinte conjunto de EventHandlers além daqueles acima. 

| Chave EventHandlers              | Tipo de mídia ou arquivo   |
|--------------------------------|----------------------|
| PlaySuperVideoCDMovieOnArrival | Super VideoCD movies |
| PlayVideoCDMovieOnArrival      | Filmes de VideoCD       |



 

 

 



