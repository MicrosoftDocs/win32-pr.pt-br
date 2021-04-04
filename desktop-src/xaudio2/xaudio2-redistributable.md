---
description: Guia do desenvolvedor para a versão redistribuível do XAudio 2.9
ms.assetid: ''
title: Guia do desenvolvedor para a versão redistribuível do XAudio 2.9
ms.topic: article
ms.date: 10/17/2019
ms.openlocfilehash: a87c2dc44179f2c189270dfa91d2cf2696ea98a7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103930248"
---
# <a name="developer-guide-for-redistributable-version-of-xaudio-29"></a>Guia do desenvolvedor para a versão redistribuível do XAudio 2.9

Uma versão do XAudio 2,9 está disponível como um [pacote NuGet](/nuget/what-is-nuget). Os desenvolvedores podem redistribuir esta versão do XAudio 2,9 com seus aplicativos. Isso permite que um aplicativo use o XAudio 2,9 em versões mais antigas do Windows que não incluem XAudio 2,9 como parte da imagem do sistema operacional. O uso desse redistribuível é preferível em relação à redistribuição de XAudio 2,7 do SDK do DirectX, já que XAudio 2,7 não foi atualizado desde 2010.

## <a name="supported-platforms"></a>Plataformas compatíveis

O pacote NuGet do XAudio 2,9 (*Microsoft. XAudio2. Redist. \* . nupkg*) inclui uma versão de 32 bits e de 64 bits de uma DLL que implementa a API do XAudio 2,9. A DLL é chamada de \_9REDIST.DLL XAudio2. Essa DLL funcionará no Windows 7 SP1, Windows 8, Windows 8.1 e Windows 10.

Quando a DLL é usada em um sistema Windows 10, ela verifica o número de versão do \_9.DLL XAudio2 que faz parte do sistema operacional e, se o sistema operacional for mais recente, ele delegará todas as chamadas à API para XAUDIO2 \_9.DLL no sistema operacional. Isso garante que os aplicativos sempre usem a versão mais recente do XAudio 2,9 que está disponível na plataforma atual.

A DLL não se destina ao Xbox One. Se usado no Xbox One, a DLL sempre delegará todas as chamadas de API para XAUDIO2 \_9.DLL no sistema operacional do Xbox One.

A DLL não se destina a aplicativos UWP. Os aplicativos UWP devem usar o \_9.DLL XAudio2 que faz parte do sistema operacional.

## <a name="installing-the-nuget-package"></a>Instalando o pacote NuGet

A maneira mais fácil de instalar o pacote NuGet é usar o [Gerenciador de pacotes NuGet](/nuget/consume-packages/install-use-packages-visual-studio) no Microsoft Visual Studio. Se você fizer isso, seu arquivo de projeto do Visual Studio será atualizado automaticamente para incluir *Microsoft. XAudio2. Redist. targets*. O arquivo *. targets* adiciona a pasta include com os arquivos de cabeçalho para o XAudio2 à sua coleção de caminhos de inclusão de projeto. O arquivo *. targets* também fará seu. DLL ou. EXE link com XAUDIO2REDIST. LIB e XAPOBASEREDIST. LIB.

A biblioteca XAPOBASEREDIST. A LIB só é necessária se você pretende impement um XAPO (objeto de processamento de XAudio) personalizado e pode removê-lo do *Microsoft. XAudio2. Redist. targets* se ele não for usado.

Você também pode usar outras ferramentas para extrair o conteúdo do pacote NuGet, ou até mesmo renomear a extensão de arquivo para. zip e extrair os arquivos com qualquer ferramenta de extrator de ZIP.

## <a name="compiling-your-app"></a>Compilando seu aplicativo

### <a name="choosing-which-headers-to-include"></a>Escolhendo quais cabeçalhos incluir

O pacote NuGet XAudio 2,9 inclui os mesmos arquivos de cabeçalho XAudio2 que estão incluídos no SDK do Windows 10. No entanto, os arquivos de cabeçalho tiveram alguns ajustes para eles para garantir que você possa usá-los, tendo como alvo explicitamente todas as [plataformas com suporte](#supported-platforms), incluindo versões mais antigas do Windows.

Se você [instalar o pacote NuGet](#installing-the-nuget-package) usando o Gerenciador de pacotes nuget no Microsoft Visual Studio, o caminho para os arquivos de cabeçalho será colocado na frente do caminho para os arquivos de cabeçalho SDK do Windows. Isso significa que, se o código em seu projeto incluir o XAUDIO2. H, ele selecionará o cabeçalho de plataforma cruzada do pacote NuGet. Esse é normalmente o comportamento desejado.

Você deve ter cuidado ao adicionar o caminho para os cabeçalhos de inclusão manualmente ao projeto, pois especificá-los na ordem errada pode causar o XAudio2 específico da versão do sistema operacional [. H](/windows/win32/api/xaudio2/) a ser incluída na SDK do Windows, em vez da versão de plataforma cruzada de XAudio2. H.

Para tornar a inclusão de cabeçalhos menos propenso a erros, o pacote NuGet contém uma versão de cada cabeçalho com "Redist" acrescentado a ele. Por exemplo, além de XAUDIO2. H, o pacote NuGet também inclui XAUDIO2REDIST. H. Se você preferir, seu código pode incluir diretamente XAUDIO2REDIST. H para eliminar qualquer ambiguidade sobre qual arquivo de cabeçalho está sendo usado. Ao incluir-Redist. A versão H de um arquivo de cabeçalho, a ordem na qual os diretórios de arquivos de inclusão são listados no arquivo de projeto não importa.

Observe que, se seu aplicativo também estiver sendo compilado para o Xbox One, você deverá continuar a incluir XAUDIO2. H ao compilar para o Xbox One, como algumas APIs específicas do Xbox One são excluídas de XAUDIO2REDIST. H. Este pacote NuGet não se destina ao Xbox One.

### <a name="loading-the-dll"></a>Carregando a DLL

Recomendamos que você vincule seu aplicativo ao XAUDIO2REDIST. LIB e instale \_ o XAUDIO29REDIST.DLL na mesma pasta que o executável do seu aplicativo. Isso fará com que \_ o XAUDIO29REDIST.DLL seja carregado assim que seu executável for iniciado. No entanto, se preferir, você pode usar [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para carregar o XAudio2 \_9REDIST.DLL sob demanda. Essa é uma boa solução se seu aplicativo nem sempre precisa usar as APIs XAudio2. Mas, se você fizer isso, deverá manter o XAUDIO2 \_9REDIST.DLL carregado até que o aplicativo saia, pois tentar descarregar a dll poderá causar uma falha se um thread em segundo plano ainda estiver executando o código na dll.

Ao contrário do XAudio 2,7 mais antigo, não é possível usar CoCreateInstance para carregar a DLL.

### <a name="verifying-the-dll-signature"></a>Verificando a assinatura da DLL

O \_ binário XAUDIO29REDIST.DLL é assinado pela Microsoft usando uma assinatura SHA-2. Qualquer código que tente validar a assinatura, por exemplo, os módulos antienganar para jogos,, portanto, precisa dar suporte ao SHA-2. Observe que o Windows 7 SP1 originalmente não dava suporte ao SHA-2 e requer uma atualização para adicionar essa funcionalidade. A atualização está disponível como [KB4474419](https://support.microsoft.com/help/4474419/sha-2-code-signing-support-update).

## <a name="testing"></a>Teste

### <a name="spatial-sound-in-newer-versions-of-windows-10"></a>Som espacial nas versões mais recentes do Windows 10

A partir da atualização do Windows 10 1903, o XAudio 2,9 usa automaticamente o [Surround Sound virtual](#spatial-sound-and-virtual-surround), se determinadas condições forem satisfeitas. É recomendável testar o jogo que gera som multicanal no Windows 10 1903 (ou mais recente) para verificar se o jogo soa como esperado.

#### <a name="enabling-spatial-sound"></a>Habilitando som espacial

O usuário pode habilitar um formato de som espacial clicando com o botão direito do mouse no ícone do palestrante na bandeja do sistema do Windows. 

XAudio 2,9 usará apenas o formato de som espacial selecionado do usuário se o processo que está usando a API XAudio2 for reconhecido como um jogo pela barra de jogos do Windows. Durante o desenvolvimento, é possível que o processo ainda não seja reconhecido como um jogo pela barra de jogos. Para alterar isso, use o atalho do teclado Win + G para abrir a barra de jogos enquanto o jogo estiver em execução. Em seguida, clique no ícone "configurações" e marque a caixa de seleção que diz "Lembre-se de que se trata de um jogo".

#### <a name="opting-out-from-spatial-sound"></a>Recusando do som espacial

Há uma maneira de recusar a XAudio2 de usar o codificador de som espacial especificando determinados valores para o parâmetro [**AUDIO_STREAM_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) em [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice). 

O som espacial está habilitado para estas categorias:

* AudioCategory_ForegroundOnlyMedia
* AudioCategory_GameEffects
* AudioCategory_GameMedia
* AudioCategory_Movie
* AudioCategory_Media

O som espacial não será habilitado se qualquer uma das seguintes categorias for especificada:

* AudioCategory_Other
* AudioCategory_Communications
* AudioCategory_Alerts
* AudioCategory_SoundEffects
* AudioCategory_GameChat
* AudioCategory_Speech

### <a name="error-handling"></a>Tratamento de erros

É importante testar que o jogo pode lidar com uma alteração no dispositivo de áudio, por exemplo, quando os fones de ouvido estão conectados ou desconectados. Isso deve ser testado com fones de ouvido que dão suporte apenas à taxa de amostragem de 44,1 kHz. Muitos fones de ouvido USB low-end e Headsets Bluetooth só dão suporte a 44,1 kHz. A transição entre a taxa de amostragem de 48 kHz e a taxa de amostragem de 44,1 kHz pode causar um erro mesmo quando o recurso de [ponto de extremidade de áudio virtual](#virtual-audio-endpoint) é usado. O erro não ocorrerá se os fones de ouvido também suportarem 48 kHz. Observe que o recurso ponto de extremidade de áudio virtual não está disponível no Windows 7 SP1.

O código de erro retornado por XAudio 2,9 quando não é possível recuperar automaticamente de uma alteração no ponto de extremidade de áudio é o [ \_ dispositivo XAudio2 E \_ \_ invalidado](xaudio2-error-codes.md). No entanto, recomendamos que os aplicativos não codifiquem uma dependência no código de erro com um valor específico.

Para ser notificado do erro, o aplicativo deve implementar a interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) e fornecer um ponteiro para essa interface invocando o método [**IXAudio2:: RegisterForCallbacks**](xaudio2-callbacks.md) . A implementação do aplicativo do [**IXAudio2EngineCallback:: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) será invocada pela API do XAudio2 se ocorrer um erro durante a reprodução.

Observe que [**IXAudio2EngineCallback:: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) não será necessariamente invocado se o pipeline de áudio estiver em pausa. Por exemplo, se o usuário minimizar o aplicativo ou se o aplicativo for suspenso por qualquer motivo, a reprodução de áudio poderá ser pausada. Se a alteração no dispositivo de áudio ocorrer durante esse tempo, o erro será retornado somente quando o aplicativo invocar [**IXAudio2:: StartEngine**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-startengine) e/ou invoca [**IXAudio2SourceVoice:: Start**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start). Se a reprodução puder ser pausada com seu aplicativo, você deverá testar a alteração do dispositivo de áudio enquanto a reprodução estiver em pausa, para verificar se o aplicativo ainda pode se recuperar dessa situação.

## <a name="xaudio-29-api-differences-compared-to-xaudio-27"></a>Diferenças de API do XAudio 2,9 em comparação com XAudio 2,7

Esta seção fornece um resumo de algumas das diferenças de API entre XAudio 2,7 e a versão redistribuível do XAudio 2,9.

### <a name="supported-formats"></a>Formatos com suporte

O XAudio 2,9 dá suporte a esses formatos de entrada no PC:

* PCM de 16 bits linear
* PCM de float de 32 bits linear
* ADPCM de 16 bits
* xWMA

O formato XMA só tem suporte no Xbox One.

### <a name="preferred-cpu-core"></a>Núcleo de CPU preferencial

É possível especificar qual CPU Core XAudio 2,9 deve usar para seu thread de processamento de áudio. No entanto, geralmente é preferível permitir que XAudio 2,9 escolha esse valor por si só. Isso é feito definindo o parâmetro **XAudio2Processor** na chamada para [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) como XAudio2 usar o \_ \_ processador padrão \_ . 

O XAudio 2,9 escolherá um núcleo de CPU diferente no Xbox, um do PC. O método IXAudio2Extension:: getprocesser pode ser usado para determinar qual XAudio2 de CPU principal foi escolhido.

### <a name="virtual-audio-endpoint"></a>Ponto de extremidade de áudio virtual

O XAudio 2,9 usará um ponto de extremidade de áudio virtual por padrão, quando executado no Windows 8 ou posterior. Isso significa que, se o ponto de extremidade de áudio padrão for alterado enquanto XAudio 2,9 for usado, ele tentará alternar automaticamente para o novo ponto de extremidade de áudio. Um exemplo de quando isso pode acontecer quando o ponto de extremidade de áudio padrão é um par de fones de ouvido conectados por USB e, em seguida, o usuário desconecta os fones de ouvido. Isso fará com que os alto-falantes sejam o novo ponto de extremidade de áudio padrão.

Se o aplicativo especificar um formato de áudio específico ao invocar [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice), talvez não seja possível para o XAudio 2,9 executar essa opção. Por exemplo, se o aplicativo especificou que a voz de mestre deve usar uma taxa de amostragem de 48 kHz e o novo dispositivo de áudio der suporte apenas a 44,1 kHz, o comutador automático falhará e o XAudio 2,9 relatará o erro [ \_ \_ \_ invalidado do dispositivo XAudio2 E](xaudio2-error-codes.md) .

É possível que o aplicativo cancele o uso do ponto de extremidade de áudio virtual passando o sinalizador [**não XAudio2 \_ de \_ \_ \_ cliente de áudio virtual**](xaudio2-boundary-values-and-flags.md) para [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

Os pontos de extremidade de áudio virtual não estão disponíveis no Windows 7 SP1. O **sinalizador \_ XAudio2 \_ nenhum \_ \_ cliente de áudio virtual** não tem nenhum efeito no Windows 7 SP1.

### <a name="audio-categories"></a>Categorias de áudio

O aplicativo deve especificar uma categoria para seu fluxo de áudio. Isso é feito fornecendo um valor da enumeração AudioCategory ao invocar o método [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) . Por exemplo, AudioCategory_GameEffects. A categoria de áudio pode afetar o modo como o Windows processa o som ou como ele representa o fluxo de áudio no painel de controle de volume. A categoria de áudio também afeta se o [surround virtual](#spatial-sound-and-virtual-surround) está habilitado automaticamente.

### <a name="duration-of-audio-processing-quantum"></a>Duração da Quantum de processamento de áudio

Na maioria dos PCs, XAudio 2,9 processa o áudio em partes de 10 milissegundos. Isso é chamado de Quantum de processamento. No entanto, a duração dessa Quantum pode ser diferente de 10 milissegundos em algum hardware. Os aplicativos que precisam saber a Quantum exata podem invocar o método IXAudio2Extension:: GetProcessingQuantum para recuperar o valor.

### <a name="spatial-sound-and-virtual-surround"></a>Som espacial e surround virtual

A partir da atualização do Windows 10 1903, o XAudio 2,9 usa automaticamente o Surround Sound virtual, se determinadas condições forem satisfeitas. É recomendável testar o jogo que gera som multicanal no Windows 10 1903 (ou mais recente) para verificar se o jogo soa como esperado. Consulte a seção [teste de som espacial](#spatial-sound-in-newer-versions-of-windows-10) para obter uma discussão sobre como testar esse recurso.

Normalmente, o XAudio 2,9 executa uma dobra de qualquer áudio de vários canais para corresponder ao número "físico" de canais de áudio que são suportados pelo ponto de extremidade de áudio. Por exemplo, se o jogo fornecer uma fonte de áudio de canal de 7,1, mas o som for reproduzido nos fones de ouvido, XAudio 2,9 dobrará o áudio do canal 7,1 em estéreo, usando uma matriz de dobras padrão do setor. Se o PC estiver conectado a um ponto de extremidade de áudio HDMI, o áudio do canal 7,1 será transmitido como está por meio da conexão HDMI.

O Windows 10 adiciona suporte para áudio espacial, usando um codificador centralizado que codifica áudio em um formato de [som espacial](../coreaudio/spatial-sound.md) selecionado pelo usuário. O Windows 10 vem incluído com um formato de som espacial chamado Windows Sonic. Outros formatos, como Dolby Atmos para fones de ouvido, podem ser baixados da Microsoft Store. Alguns dos formatos de som espaciais, como o Windows Sonic e o Dolby Atmos para fones de ouvido, foram projetados para serem usados em pontos de extremidade de áudio estéreo. Esses formatos dobram o som surround para o estéreo usando algoritmos proprietários que atingem um efeito de som surround "virtual". Em outras palavras, o ouvinte pode perceber que o som aparecesse de diferentes posições no espaço 3D mesmo enquanto estiver apenas gastando fones de ouvido ou escutando em um único par de auto-falantes estéreo.

Efeitos semelhantes podem ser obtidos usando as APIs [X3DAudio](x3daudio.md) incluídas no XAudio 2,9. A principal diferença é que o X3DAudio exige que o desenvolvedor do aplicativo programe explicitamente para áudio 3D, enquanto que o surround virtual é aplicado automaticamente a qualquer fonte de som baseada em canal tradional.

No Windows 10 1903 e mais recentes, os jogos que usam o XAudio 2,9 usarão o formato de som espacial de todo o sistema que o usuário habilitou no ponto de extremidade de áudio, se houver. Isso significa que o XAudio 2,9 não executará a dobra normal do som surround para o estéreo. Em vez disso, o sinal de som surround será entregue ao codificador de som espacial (por exemplo, o Windows Sonic) para obter um efeito surround virtual.

### <a name="createhrtfapo"></a>CreateHrtfApo

A função [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) só está disponível no Windows 10. Ele não é implementado no XAudio 2,9 redistribuível.
