---
title: Abrindo um dispositivo
description: Abrindo um dispositivo
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- MCI_OPEN comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007397"
---
# <a name="opening-a-device"></a>Abrindo um dispositivo

Antes de usar um dispositivo, você deve inicializá-lo usando o comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)). Esse comando carrega o driver na memória (se ele ainda não estiver carregado) e recupera o identificador de dispositivo que você usará para identificar o dispositivo em comandos MCI subsequentes. Você deve verificar o valor de retorno da função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) ou [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) antes de usar um novo identificador de dispositivo para garantir que o identificador seja válido. (Você também pode recuperar um identificador de dispositivo usando a função [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) .)

Como todas as mensagens de comando MCI, o **MCI \_ Open** tem uma estrutura associada. Essas estruturas são, às vezes, chamadas de *blocos de parâmetro*. A estrutura padrão para o **MCI \_ Open** é o [**MCI \_ Open \_ parms**](mci-open-parms.md). Determinados dispositivos (como forma de *onda* e *sobreposição*) têm estruturas estendidas (como o [**MCI \_ Wave \_ Open \_ parms**](mci-wave-open-parms.md) e o [**MCI \_ OVLY \_ Open \_ parms**](mci-ovly-open-parms.md)) para acomodar parâmetros opcionais adicionais. A menos que você precise usar esses parâmetros adicionais, poderá usar a estrutura **MCI \_ Open \_ parms** com qualquer dispositivo MCI.

O número de dispositivos que você pode ter aberto é limitado apenas pela quantidade de memória disponível.

## <a name="using-an-alias"></a>Usando um alias

Ao abrir um dispositivo, você pode usar o sinalizador "alias" para especificar um identificador de dispositivo para o dispositivo. Esse sinalizador permite que você atribua um pequeno identificador de dispositivo para dispositivos compostos com nomes de arquivo longos e permite abrir várias instâncias do mesmo arquivo ou dispositivo.

Por exemplo, o comando a seguir atribui o identificador de dispositivo "birdcall" ao nome de arquivo longo: \\ NABIRDS \\ sons \\ MOCKMTNG. WAV


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Na interface de mensagem de comando, você especifica um alias usando o membro **lpstrAlias** da estrutura de [**\_ \_ parâmetros abertos do MCI**](mci-open-parms.md) .

## <a name="specifying-a-device-type"></a>Especificando um tipo de dispositivo

Ao abrir um dispositivo, você pode usar o sinalizador "tipo" para se referir a um tipo de dispositivo, e não a um driver de dispositivo específico. O exemplo a seguir abre o arquivo de formato de onda-áudio C: \\ Windows \\ Chimes. WAV (usando o sinalizador "Type" para especificar o tipo de dispositivo **WaveAudio** ) e atribui o alias "Chimes":


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Na interface de mensagem de comando, a funcionalidade do sinalizador "Type" é fornecida pelo membro **lpstrDeviceType** da estrutura [**MCI \_ Open \_ parms**](mci-open-parms.md) .

## <a name="simple-and-compound-devices"></a>Dispositivos simples e compostos

O MCI classifica os drivers de dispositivo como *compostos* ou *simples*. Os drivers para dispositivos compostos exigem o nome de um arquivo de dados para reprodução; os drivers para dispositivos simples não fazem isso.

Dispositivos simples incluem dispositivos **cdaudio** e **VIDEODISC** . Há duas maneiras de abrir dispositivos simples:

-   Especifique um ponteiro para uma cadeia de caracteres terminada em nulo que contenha o nome do dispositivo do registro ou o arquivo de SYSTEM.INI.

    Por exemplo, você pode abrir um dispositivo **VIDEODISC** usando o seguinte comando:


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



Nesse caso, "VIDEODISC" é o nome do dispositivo no registro ou na \[ seção MCI \] de SYSTEM.INI.

-   Especifique o nome real do driver de dispositivo. No entanto, abrir um dispositivo usando o nome de arquivo do driver do dispositivo torna o aplicativo específico ao dispositivo e pode impedir que o aplicativo seja executado se a configuração do sistema for alterada. Se você usar um nome de arquivo, não será necessário especificar o caminho completo ou a extensão de nome de arquivo; O MCI pressupõe que os drivers estejam localizados em um diretório do sistema e tenham o. Extensão de nome de arquivo DRV.

Os dispositivos compostos incluem dispositivos **WaveAudio** e **Sequencer** . Os dados de um dispositivo composto, às vezes, são chamados de um *elemento de dispositivo*. Esse documento, no entanto, geralmente se refere a esses dados como um arquivo, embora, em alguns casos, os dados possam não ser armazenados como um arquivo.

Há três maneiras de abrir um dispositivo composto:

-   Especifique apenas o nome do dispositivo. Isso permite que você abra um dispositivo composto sem associar um nome de arquivo. A maioria dos dispositivos compostos processa apenas os comandos de [**capacidade**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) e [**fechar**](close.md) ([**MCI \_ fechar**](mci-close.md)) quando eles são abertos dessa maneira.
-   Especifique somente o nome do arquivo. O nome do dispositivo é determinado das associações no registro.
-   Especifique o nome do arquivo e do dispositivo. O MCI ignora as entradas no registro e abre o nome do dispositivo especificado.

Para associar um arquivo de dados a um dispositivo específico, você pode especificar o nome do arquivo e do dispositivo. Por exemplo, o comando a seguir abre o dispositivo **WaveAudio** com o nome de arquivo myvoice. SND


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Na interface de cadeia de caracteres de comando, você também pode abreviar a especificação do nome do dispositivo usando o formato de ponto de exclamação alternativo, conforme documentado com o comando [**abrir**](open.md) .

## <a name="opening-a-device-using-the-filename-extension"></a>Abrindo um dispositivo usando a extensão de nome de arquivo

Se o comando [**abrir**](open.md) ([**MCI \_ aberto**](mci-open.md)) especificar apenas o nome do arquivo, o MCI usará a extensão de nome de arquivo para selecionar o dispositivo apropriado na lista no registro ou na \[ seção de extensões MCI \] do arquivo de SYSTEM.INI. As entradas na \[ seção de extensões MCI \] usam o seguinte formato:

nome do dispositivo de *\_ extensão de nome de arquivo*  =  *\_*

O MCI usa implicitamente o *\_ nome do dispositivo* se a extensão for encontrada e se um nome de dispositivo não tiver sido especificado no comando **Open** .

O exemplo a seguir mostra uma \[ seção típica de extensões MCI \] :


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



Usando essas definições, o MCI abrirá o dispositivo **WaveAudio** se o seguinte comando for emitido:


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a>Novos arquivos de dados

Para criar um novo arquivo de dados, basta especificar um nome de arquivo em branco. O MCI não salva um novo arquivo até que você o salve usando o comando [**salvar**](save.md) ([**\_ salvar como MCI**](mci-save.md)). Ao criar um novo arquivo, você deve incluir um alias de dispositivo com o comando [**abrir**](open.md) ([**MCI \_ aberto**](mci-open.md)).

O exemplo a seguir abre um novo arquivo **WaveAudio** , inicia e interrompe a gravação e, em seguida, salva e fecha o arquivo:


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

O sinalizador "compartilhável" (MCI \_ Open \_ Shareable) do comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)) permite que vários aplicativos acessem o mesmo dispositivo (ou arquivo) e instância de dispositivo simultaneamente. Se seu aplicativo abrir um dispositivo ou arquivo como compartilhável, outros aplicativos também poderão acessá-lo, abrindo-o como compartilhável. O dispositivo ou arquivo compartilhado fornece a cada aplicativo a capacidade de alterar os parâmetros que regem seu estado operacional. Cada vez que um dispositivo ou arquivo é aberto como compartilhável, o MCI retorna um identificador de dispositivo exclusivo, embora os identificadores façam referência à mesma instância.

Se seu aplicativo abrir um dispositivo ou arquivo sem especificar que ele é compartilhável, nenhum outro aplicativo poderá acessá-lo até que seu aplicativo o feche. Além disso, se um dispositivo der suporte a apenas uma instância aberta, o comando **abrir** falhará se você especificar o sinalizador compartilhável.

Se seu aplicativo abrir um dispositivo e especificar que ele pode ser compartilhado, seu aplicativo não deverá fazer suposições sobre o estado desse dispositivo. Seu aplicativo pode precisar compensar as alterações feitas por outros aplicativos que acessam o dispositivo.

A maioria dos arquivos compostos não é compartilhável; no entanto, você pode abrir vários arquivos ou pode abrir um único arquivo várias vezes. Se você abrir um único arquivo várias vezes, o MCI criará uma instância independente para cada uma, com cada instância com um status operacional exclusivo.

Se você abrir várias instâncias de um arquivo, deverá atribuir um identificador de dispositivo exclusivo a cada uma. Você pode usar um alias, conforme descrito na seção a seguir, para atribuir um nome exclusivo para cada arquivo.

 

 