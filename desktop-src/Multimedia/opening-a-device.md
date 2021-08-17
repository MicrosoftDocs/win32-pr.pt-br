---
title: Abrindo um dispositivo
description: Abrindo um dispositivo
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- MCI_OPEN comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34408cef4e85ed7200b91c610e60ca546ff488ce5ad45edee12159a664f319fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802313"
---
# <a name="opening-a-device"></a>Abrindo um dispositivo

Antes de usar um dispositivo, você deve inicializá-lo usando o [**comando open**](open.md) ([**MCI \_ OPEN**](mci-open.md)). Esse comando carrega o driver na memória (se ele ainda não estiver carregado) e recupera o identificador de dispositivo que você usará para identificar o dispositivo em comandos MCI subsequentes. Você deve verificar o valor de retorno da [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) ou [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) antes de usar um novo identificador de dispositivo para garantir que o identificador seja válido. (Você também pode recuperar um identificador de dispositivo usando a [**função mciGetDeviceID.)**](/previous-versions//dd757156(v=vs.85))

Como todas as mensagens de comando MCI, **o MCI \_ OPEN** tem uma estrutura associada. Às vezes, essas estruturas são chamadas *de blocos de parâmetro.* A estrutura padrão para **MCI \_ OPEN** é [**MCI \_ OPEN \_ PARMS.**](mci-open-parms.md) Determinados dispositivos (como *waveform* e *overlay*) têm estruturas estendidas (como [**MCI \_ WAVE OPEN \_ \_ PARMS**](mci-wave-open-parms.md) e [**MCI \_ OVLY \_ OPEN \_ PARMS**](mci-ovly-open-parms.md)) para acomodar parâmetros opcionais adicionais. A menos que você precise usar esses parâmetros adicionais, você pode usar a estrutura **MCI \_ OPEN \_ PARMS** com qualquer dispositivo MCI.

O número de dispositivos que você pode ter aberto é limitado apenas pela quantidade de memória disponível.

## <a name="using-an-alias"></a>Usando um alias

Ao abrir um dispositivo, você pode usar o sinalizador "alias" para especificar um identificador de dispositivo para o dispositivo. Esse sinalizador permite atribuir um identificador de dispositivo curto para dispositivos compostos com nomes de arquivo longos e permite que você abra várias instâncias do mesmo arquivo ou dispositivo.

Por exemplo, o comando a seguir atribui o identificador de dispositivo "birdcall" ao nome de arquivo longo C: \\ NABIRDS \\ SOUNDS \\ MOCKMTNG. Wav:


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Na interface de mensagem de comando, especifique um alias usando o **membro lpstrAlias** da [**estrutura MCI OPEN \_ \_ PARMS.**](mci-open-parms.md)

## <a name="specifying-a-device-type"></a>Especificando um tipo de dispositivo

Ao abrir um dispositivo, você pode usar o sinalizador "tipo" para se referir a um tipo de dispositivo, em vez de a um driver de dispositivo específico. O exemplo a seguir abre o arquivo waveform-audio C: \\ WINDOWS \\ CHIMES. WAV (usando o sinalizador "type" para especificar o tipo de dispositivo **waveaudio)** e atribui o alias "chimes":


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Na interface de mensagem de comando, a funcionalidade do sinalizador "type" é fornecida pelo membro **lpstrDeviceType** da estrutura [**MCI \_ OPEN \_ PARMS.**](mci-open-parms.md)

## <a name="simple-and-compound-devices"></a>Dispositivos simples e compostos

A MCI classifica os drivers de dispositivo como *compostos* ou *simples.* Os drivers para dispositivos compostos exigem o nome de um arquivo de dados para reprodução; drivers para dispositivos simples não.

Dispositivos simples **incluem dispositivos cdaudio** **e videodisc.** Há duas maneiras de abrir dispositivos simples:

-   Especifique um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do dispositivo do Registro ou o SYSTEM.INI arquivo.

    Por exemplo, você pode abrir um **dispositivo videodisc** usando o seguinte comando:


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



Nesse caso, "videodisc" é o nome do dispositivo do Registro ou da \[ seção mci \] do SYSTEM.INI.

-   Especifique o nome real do driver de dispositivo. Abrir um dispositivo usando o nome de arquivo do driver de dispositivo, no entanto, torna o aplicativo específico do dispositivo e pode impedir que o aplicativo seja executado se a configuração do sistema for mudada. Se você usar um nome de arquivo, não precisará especificar o caminho completo ou a extensão de nome de arquivo; A MCI presume que os drivers estão localizados em um diretório do sistema e têm o . Extensão de nome de arquivo DRV.

Os dispositivos compostos **incluem dispositivos waveaudio** **e sequencer.** Às vezes, os dados de um dispositivo composto são chamados de *elemento de dispositivo*. Este documento, no entanto, geralmente se refere a esses dados como um arquivo, embora, em alguns casos, os dados possam não ser armazenados como um arquivo.

Há três maneiras de abrir um dispositivo composto:

-   Especifique apenas o nome do dispositivo. Isso permite que você abra um dispositivo composto sem associar um nome de arquivo. A maioria dos dispositivos compostos processa apenas a funcionalidade [**(**](capability.md) [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) e fecha [**os**](close.md) comandos ([**MCI \_ CLOSE**](mci-close.md)) quando eles são abertos dessa maneira.
-   Especifique apenas o nome do arquivo. O nome do dispositivo é determinado com base nas associações no Registro.
-   Especifique o nome do arquivo e o nome do dispositivo. A MCI ignora as entradas no Registro e abre o nome do dispositivo especificado.

Para associar um arquivo de dados a um dispositivo específico, você pode especificar o nome do arquivo e o nome do dispositivo. Por exemplo, o comando a seguir abre o **dispositivo waveaudio** com o nome de arquivo MYVOICE. Snd:


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Na interface de cadeia de caracteres de comando, você também pode abreviar a especificação de nome do dispositivo usando o formato de ponto de exclamação alternativo, conforme documentado com [**o comando open.**](open.md)

## <a name="opening-a-device-using-the-filename-extension"></a>Abrindo um dispositivo usando a extensão filename

Se o comando [**open**](open.md) ([**MCI \_ OPEN**](mci-open.md)) especificar apenas o nome do arquivo, a MCI usará a extensão filename para selecionar o dispositivo apropriado na lista no registro ou na seção de extensões mci do arquivo \[ SYSTEM.INI \] arquivo. As entradas na seção \[ de extensões mci \] usam o seguinte formulário:

*nome do dispositivo \_ de extensão filename*  =  *\_*

A MCI usará implicitamente o nome do dispositivo se a extensão for encontrada e se um nome de dispositivo não tiver sido especificado no **comando** open. *\_*

O exemplo a seguir mostra uma seção \[ típica de extensões \] mci:


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



Usando essas definições, a MCI abrirá o **dispositivo waveaudio** se o seguinte comando for emitido:


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a>Novos arquivos de dados

Para criar um novo arquivo de dados, basta especificar um nome de arquivo em branco. A MCI não salva um novo arquivo até que você o salve usando [**o comando salvar**](save.md) ([**MCI \_ SAVE**](mci-save.md)). Ao criar um novo arquivo, você deve incluir um alias de dispositivo com o [**comando open**](open.md) ([**MCI \_ OPEN**](mci-open.md)).

O exemplo a seguir abre um novo **arquivo waveaudio,** inicia e interrompe a gravação e, em seguida, salva e fecha o arquivo:


```C++
mciSendString("open new type waveaudio alias capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("record capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("stop capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("save capture orca.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="sharable-devices"></a>Dispositivos compartilháveis

O sinalizador "compartilhável" (MCI OPEN SHAREABLE) do comando open ( MCI OPEN ) permite que vários aplicativos acessem o mesmo dispositivo (ou arquivo) e a instância do \_ \_ dispositivo simultaneamente.[**\_**](mci-open.md) [](open.md) Se seu aplicativo abrir um dispositivo ou arquivo como compartilhável, outros aplicativos também poderão acessá-lo abrindo-o como compartilhável. O dispositivo ou arquivo compartilhado oferece a cada aplicativo a capacidade de alterar os parâmetros que regem seu estado operacional. Sempre que um dispositivo ou arquivo é aberto como compartilhável, a MCI retorna um identificador de dispositivo exclusivo, mesmo que os identificadores se refiram à mesma instância.

Se seu aplicativo abrir um dispositivo ou arquivo sem especificar que ele é compartilhável, nenhum outro aplicativo poderá acessá-lo até que seu aplicativo o feche. Além disso, se um dispositivo dá  suporte a apenas uma instância aberta, o comando open falhará se você especificar o sinalizador compartilhável.

Se seu aplicativo abrir um dispositivo e especificar que ele é compartilhável, seu aplicativo não deverá fazer suposições sobre o estado desse dispositivo. Seu aplicativo pode precisar compensar as alterações feitas por outros aplicativos que acessam o dispositivo.

A maioria dos arquivos compostos não é compartilhável; no entanto, você pode abrir vários arquivos ou abrir um único arquivo várias vezes. Se você abrir um único arquivo várias vezes, a MCI criará uma instância independente para cada uma delas, com cada instância com um status operacional exclusivo.

Se você abrir várias instâncias de um arquivo, deverá atribuir um identificador de dispositivo exclusivo a cada um. Você pode usar um alias, conforme descrito na seção a seguir, para atribuir um nome exclusivo para cada arquivo.

 

 