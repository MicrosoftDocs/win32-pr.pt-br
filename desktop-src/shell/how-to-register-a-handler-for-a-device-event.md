---
description: Descreve os processos para implementar manipuladores de eventos de dispositivo no Registro.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Como registrar um manipulador para um evento de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a13abe8917d93ac6a4801e0c11cb7223da25e362923df229180b8c8e6211ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859595"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a>Como registrar um manipulador para um evento de dispositivo

Os manipuladores definem a parte de software do AutoPlay. Eles definem o ícone do software e o nome amigável, bem como o componente Component Object Model (COM) para insinciar e como inicializar o componente em resposta a um evento. Cada manipulador para um evento específico é registrado como um valor sob a **chave EventHandler** apropriada. Quando esse evento é detectado, o usuário é solicitado a escolher um manipulador em uma lista de todos os manipuladores registrados para esse evento.

## <a name="instructions"></a>Instruções


Manipuladores e seus valores associados são definidos na **chave Manipuladores AutoplayHandlers.** \\  As sub-chaves diferem dependendo se o sistema pode ler o conteúdo do dispositivo diretamente ou se o dispositivo fornece conteúdo para o sistema por meio de uma interface proprietária.

O exemplo a seguir mostra as sub-chaves e os valores usados para um dispositivo, como uma câmera de vídeo digital ou um player .mp3, que fornece seu conteúdo para o sistema por meio de uma interface proprietária. O manipulador de exemplo é chamado **MyHandler.**

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
> Embora o exemplo mostre um valor ProgID e um CLSID (identificador de classe), na prática, esses valores são mutuamente exclusivos para que apenas um ou outro seja presente. O valor progID é preferencial. O que for usado, ele deverá apontar para um componente COM que implementa a interface [**IHWEventHandler.**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

 

Você pode inserir o valor Ação como um valor literal, por exemplo, "Reproduzir música", conforme mostrado neste exemplo, ou como um nome de arquivo com uma cadeia de caracteres de recurso. Você também pode inserir o valor provedor como um valor literal ou como um nome de arquivo com uma cadeia de caracteres de recurso. A Reprodução Automática combina o valor ação e o valor do Provedor com a palavra "using" para criar uma legenda amigável que é exibida na interface do usuário. No exemplo, a legenda resultante é "Reproduzir música usando Windows Media Player".

O valor DefaultIcon aponta para um arquivo .ico ou um recurso em um arquivo binário. Se o valor numérico que segue o nome do arquivo binário for zero ou maior, ele será o valor de índice do ícone nesse arquivo binário. Se for um valor negativo, será a ID do recurso de ícone. Valores de índice negativos são recomendados. Nenhum valor é necessário no caso de um arquivo .ico. É recomendável usar variáveis de ambiente no caminho.

O valor initCmdLine passa inalterado pelo método [**IHWEventHandler::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) antes de qualquer outro método ser chamado.

O exemplo a seguir mostra as sub-chaves e os valores usados para um dispositivo que pode ser lido diretamente, como uma unidade CD-ROM ou outro disco removível. Novamente, o manipulador de exemplo é chamado **MyHandler**.

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

Neste exemplo, os valores de Ação e Provedor são mostrados como um nome de arquivo com uma cadeia de caracteres de recurso em vez de valores literais, mas as cadeias de caracteres referenciadas são usadas da mesma maneira. Eles são combinados com a palavra "using" para formar uma legenda amigável, conforme explicado anteriormente.

Os valores InvokeProgID e InvokeVerb substituem CLSID, InitCmdLine e ProgID. Os valores InvokeProgID e InvokeVerb são os nomes de chave encontrados em **HKEY \_ CLASSES \_ ROOT,** conforme mostrado na entrada do Registro a seguir. Esse conjunto de chaves de exemplo corresponde ao exemplo de Manipulador específico descrito anteriormente.

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

A [**função CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) usa o CLSID para implementar o aplicativo apropriado.

Depois de definir o manipulador de qualquer uma dessas duas maneiras, você precisará registrá-lo para um evento específico. Faça isso fornecendo o nome do manipulador como um valor para a chave desse evento em **EventHandlers.** O exemplo a seguir mostra como registrar **MyHandler** como um manipulador para o evento GenericVolumeArrival. Ele não tem nenhum valor de dados atribuído.

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

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
