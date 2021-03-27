---
description: Descreve os processos para implementar manipuladores de eventos de dispositivo no registro.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Como registrar um manipulador para um evento de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef15071b349afa3f863e7c57b64c280c2aef8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828289"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a>Como registrar um manipulador para um evento de dispositivo

Os manipuladores definem a parte do software da reprodução automática. Eles definem o ícone do software e o nome amigável, bem como o componente de Component Object Model (COM) para instanciar e como inicializar o componente em resposta a um evento. Cada manipulador de um evento específico é registrado como um valor na chave **EventHandler** apropriada. Quando esse evento é detectado, o usuário é solicitado a escolher um manipulador de uma lista de todos os manipuladores registrados para esse evento.

## <a name="instructions"></a>Instruções


Os manipuladores e seus valores associados são definidos sob a chave de \\ **manipuladores** AutoplayHandlers. As subchaves diferem dependendo se o sistema pode ler o conteúdo do dispositivo diretamente ou se o dispositivo fornece conteúdo ao sistema por meio de uma interface proprietária.

O exemplo a seguir mostra as subchaves e os valores que são usados para um dispositivo, como uma câmera de vídeo digital ou um player de MP3, que fornece seu conteúdo ao sistema por meio de uma interface proprietária. O manipulador de exemplo é chamado de **MyHandler**.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = Play music
                           CLSID [REG_SZ] = {a51f2ed3-634e-4a97-9d55-efcf08e7b32f}
                           DefaultIcon [REG_EXPAND_SZ] = %ProgramFiles%\Windows Media Player\wmplayer.exe,0
                           InitCmdLine [REG_SZ] = /Play
                           ProgID [REG_SZ] = WMP.PlayMusicFiles
                           Provider [REG_SZ] = Windows Media Player
```

> [!Note]  
> Embora o exemplo mostre um ProgID e um valor de identificador de classe (CLSID), na prática, esses valores são mutuamente exclusivos para que apenas um ou outro esteja presente. O valor de ProgID é preferencial. Seja qual for o uso, ele deve apontar para um componente COM que implementa a interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .

 

Você pode inserir o valor da ação como um valor literal, por exemplo, "reproduzir música", conforme mostrado neste exemplo, ou como um nome de arquivo com uma cadeia de caracteres de recurso. Você também pode inserir o valor do provedor como um valor literal ou como um nome de arquivo com uma cadeia de caracteres de recurso. A reprodução automática combina o valor da ação e o valor do provedor com a palavra "usando" para criar uma legenda amigável que é exibida na interface do usuário. No exemplo, a legenda resultante é "reproduzir música usando o Windows Media Player".

O valor de DefaultIcon aponta para um arquivo. ico ou um recurso em um arquivo binário. Se o valor numérico que segue o nome do arquivo binário for zero ou maior, será o valor de índice do ícone nesse arquivo binário. Se for um valor negativo, será o ícone ID de recurso. São recomendados valores de índice negativos. Nenhum valor é necessário no caso de um arquivo. ico. É recomendável que você use variáveis de ambiente no caminho.

O valor InitCmdLine passa inalterado por meio do método [**IHWEventHandler:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) antes de qualquer outro método ser chamado.

O exemplo a seguir mostra as subchaves e os valores que são usados para um dispositivo que pode ser lido diretamente, como uma unidade de CD-ROM ou outro disco removível. Novamente, o manipulador de exemplo é chamado de **MyHandler**.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-276
                           DefaultIcon [REG_EXPAND_SZ] = %systemroot%\System32\wiaacmgr.exe,-2
                           InvokeProgID [REG_SZ] = WIA.AutoPlayDropHandler
                           InvokeVerb [REG_SZ] = open
                           Provider [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-101
```

Neste exemplo, os valores de ação e provedor são mostrados como um nome de arquivo com uma cadeia de caracteres de recurso em vez de valores literais, mas as cadeias de caracteres que eles referenciam são usadas da mesma maneira. Eles são combinados com a palavra "usando" para formar uma legenda amigável, conforme explicado anteriormente.

Os valores InvokeProgID e InvokeVerb substituem CLSID, InitCmdLine e ProgID. Os valores InvokeProgID e InvokeVerb correspondem aos nomes de chave encontrados na **\_ \_ raiz de classes hKey**, conforme mostrado na entrada de registro a seguir. Esse conjunto de chaves de exemplo corresponde ao exemplo de manipulador específico descrito anteriormente.

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

A função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) usa o CLSID para implementar o aplicativo apropriado.

Depois de definir o manipulador de uma dessas duas maneiras, você precisa registrá-lo para um evento específico. Você faz isso fornecendo o nome do manipulador como um valor para a chave do evento em **EventHandlers**. O exemplo a seguir mostra como registrar **MyHandler** como um manipulador para o evento GenericVolumeArrival. Ele não tem nenhum valor de dados atribuído.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        GenericVolumeArrival
                           MyHandler [REG_SZ]
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
