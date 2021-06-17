---
description: Guia do desenvolvedor para a versão redistribuível do XAudio 2.9
ms.assetid: ''
title: Guia do desenvolvedor para a versão redistribuível do XAudio 2.9
ms.topic: article
ms.date: 10/17/2019
ms.openlocfilehash: a73ebd01d599446dc96e1e6735d8af572203a23b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262588"
---
# <a name="developer-guide-for-redistributable-version-of-xaudio-29"></a>Guia do desenvolvedor para a versão redistribuível do XAudio 2.9

Uma versão do XAudio 2.9 está disponível como um [pacote NuGet](/nuget/what-is-nuget). Os desenvolvedores podem redistribuir essa versão do XAudio 2.9 com seus aplicativos. Isso permite que um aplicativo use o XAudio 2.9 em versões mais antigas do Windows que não incluem o XAudio 2.9 como parte da imagem do sistema operacional. O uso desse redistribuível é preferencial em vez de redistribuir o XAudio 2.7 do SDK do DirectX, pois o XAudio 2.7 não foi atualizado desde 2010.

Visite a Página de [Aterrissagem do DirectX para](https://devblogs.microsoft.com/directx/landing-page/) obter mais recursos para desenvolvedores do DirectX.

## <a name="supported-platforms"></a>Plataformas compatíveis

O pacote NuGet XAudio 2.9 (*Microsoft.XAudio2.Redist. \* . nupkg*) inclui uma versão de 32 bits e uma versão de 64 bits de uma DLL que implementa a API XAudio 2.9. A DLL é chamada de XAUDIO2 \_9REDIST.DLL. Essa DLL funcionará no Windows 7 SP1, Windows 8, Windows 8.1 e Windows 10.

Quando a DLL é usada em um sistema Windows 10, ela verifica o número de versão do9.DLL XAUDIO2 que faz parte do sistema operacional e, se o sistema operacional for mais recente, ele delegará todas as chamadas à API para o9.DLL \_ XAUDIO2 no sistema \_ operacional. Isso garante que os aplicativos sempre usem a versão mais recente do XAudio 2.9 que está disponível na plataforma atual.

A DLL não se destina a Xbox One. Se usado no Xbox One, a DLL sempre delegará todas as chamadas à API para9.DLL XAUDIO2 no \_ Xbox One operacional.

A DLL não se destina a aplicativos UWP. Os aplicativos UWP devem usar o9.DLL XAUDIO2 \_ que faz parte do sistema operacional.

## <a name="installing-the-nuget-package"></a>Instalando o pacote NuGet

A maneira mais fácil de instalar o pacote NuGet é usar o [Gerenciador de Pacotes NuGet](/nuget/consume-packages/install-use-packages-visual-studio) Microsoft Visual Studio. Se você fizer isso, o Visual Studio de projeto será atualizado automaticamente para incluir *Microsoft.XAudio2.Redist.targets.* O *arquivo .targets* adiciona a pasta Include com os arquivos de header do XAudio2 à sua coleção de caminhos de inclusão de projeto. O *arquivo .targets* também fará com que seu .DLL ou .EXE link com XAUDIO2REDIST. LIB e XAPOBASEREDIST. Lib.

A biblioteca XAPOBASEREDIST. LIB só será necessário se você pretende empalar um objeto de processamento XAudio personalizado (XAPO) e você pode removê-lo do *Microsoft.XAudio2.Redist.targets* se ele não for usado.

Você também pode usar outras ferramentas para extrair o conteúdo do pacote NuGet ou até mesmo renomear a extensão de arquivo para .zip e extrair os arquivos com qualquer ferramenta de extrator zip.

> Também há uma ``xaudio2redist`` porta disponível para o [vc++ Gerenciador de Pacotes](https://github.com/microsoft/vcpkg).

## <a name="compiling-your-app"></a>Compilando seu aplicativo

### <a name="choosing-which-headers-to-include"></a>Escolhendo quais headers incluir

O pacote NuGet XAudio 2.9 inclui os mesmos arquivos de header XAudio2 incluídos no SDK do Windows 10. No entanto, os arquivos de header tiveram alguns ajustes para garantir que você possa usá-los ao direcionar explicitamente todas as [plataformas](#supported-platforms)com suporte, incluindo versões mais antigas do Windows.

Se você instalar o pacote [NuGet](#installing-the-nuget-package) usando o Gerenciador de Pacotes NuGet no Microsoft Visual Studio, o caminho para os arquivos de header será colocado na frente do caminho para os arquivos de SDK do Windows de SDK do Windows. Isso significa que se o código em seu projeto incluir o XAUDIO2. O header H, ele escolherá o header de plataforma cruzada do pacote NuGet. Normalmente, esse é o comportamento desejado.

Você deve ter cuidado se adicionar o caminho aos headers de inclusão manualmente ao projeto, pois especificá-los na ordem errada pode causar o XAUDIO2 específico da versão do sistema [operacional. H](/windows/win32/api/xaudio2/) a ser incluído do SDK do Windows, em vez da versão de plataforma cruzada do XAUDIO2.H.

Para tornar a inclusão de headers menos propensa a erros, o pacote NuGet contém uma versão de cada header com "REDIST" anexado a ele. Por exemplo, além de XAUDIO2. H, o pacote NuGet também inclui XAUDIO2REDIST.H. Se preferir, seu código poderá incluir diretamente XAUDIO2REDIST. H para eliminar qualquer ambiguidade sobre qual arquivo de header está sendo usado. Ao incluir o -REDIST. A versão H de um arquivo de header, a ordem na qual os diretórios de arquivos de inclusão são listados no arquivo de projeto, não importa.

Observe que, se seu aplicativo também estiver sendo compilado para Xbox One, você deverá continuar a incluir o XAUDIO2. H ao compilar para Xbox One, pois algumas APIs específicas Xbox One são excluídas de XAUDIO2REDIST.H. Este pacote NuGet não se destina a Xbox One.

### <a name="loading-the-dll"></a>Carregando a DLL

Recomendamos que você vincule seu aplicativo ao XAUDIO2REDIST. LIB e instale o XAUDIO2 \_9REDIST.DLL na mesma pasta que o executável do aplicativo. Isso fará com que o9REDIST.DLL XAUDIO2 \_ seja carregado assim que o executável for lançado. No entanto, se preferir, você poderá usar [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para carregar9REDIST.DLL XAUDIO2 \_ sob demanda. Essa é uma boa solução se seu aplicativo nem sempre precisa usar as APIs XAudio2. Mas se você fizer isso, deverá manter o XAUDIO29REDIST.DLL carregado até que o aplicativo saia, pois tentar descarregar a DLL poderá causar uma falha se um thread em segundo plano ainda estiver executando o código na \_ DLL.

Ao contrário do XAudio 2.7 mais antigo, não é possível usar CoCreateInstance para carregar a DLL.

### <a name="verifying-the-dll-signature"></a>Verificando a assinatura de DLL

O binário de9REDIST.DLL XAUDIO2 \_ é assinado pela Microsoft usando uma assinatura SHA-2. Qualquer código que tenta validar a assinatura, por exemplo, módulos anti-cheat para jogos, portanto, precisa dar suporte ao SHA-2. Observe que o Windows 7 SP1 não era originalmente suportado sha-2 e requer uma atualização para adicionar essa funcionalidade. A atualização está disponível como [KB4474419](https://support.microsoft.com/help/4474419/sha-2-code-signing-support-update).

## <a name="testing"></a>Testando

### <a name="spatial-sound-in-newer-versions-of-windows-10"></a>Som espacial em versões mais recentes do Windows 10

A partir da atualização Windows 10 1903, o XAudio 2.9 usa automaticamente o som [de surround virtual](#spatial-sound-and-virtual-surround), se determinadas condições são atendidas. É recomendável testar o jogo que gera som de vários canais no Windows 10 1903 (ou mais novo) para verificar se o jogo parece o esperado.

#### <a name="enabling-spatial-sound"></a>Habilitando o som espacial

O usuário pode habilitar um formato de som espacial clicando com o botão direito do mouse no ícone do locutor na bandeja do sistema Windows. 

O XAudio 2.9 só usará o formato de som espacial selecionado pelo usuário se o processo que está usando a API XAudio2 for reconhecido como um jogo pelo Windows Game Bar. Durante o desenvolvimento, é possível que o processo ainda não seja reconhecido como um jogo pelo Game Bar. Para alterar isso, use o atalho do teclado Win+G para abrir o Game Bar enquanto o jogo está em execução. Em seguida, clique no ícone "Configurações" e marque a caixa de seleção que diz " Lembre-se de que este é um jogo".

#### <a name="opting-out-from-spatial-sound"></a>Opting out from spatial sound

Há uma maneira de não fazer com que XAudio2 use o codificador de som espacial especificando determinados valores para o parâmetro [**AUDIO_STREAM_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) em [**IXAudio2::CreateMasteringVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) 

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

É importante testar se o jogo pode lidar com uma alteração no dispositivo de áudio, por exemplo, quando os fones de ouvido estão conectados ou desconectados. Isso deve ser testado com fones de ouvido que só suportam taxa de amostragem de 44,1 kHz. Muitos fones de ouvido USB de baixo nível e headsets Bluetooth só são compatíveis com 44,1 kHz. A transição entre a taxa de amostragem de 48 kHz e a taxa de amostragem de 44,1 kHz pode causar um erro mesmo quando o recurso de ponto de extremidade de áudio [virtual](#virtual-audio-endpoint) é usado. O erro não ocorrerá se os fones de ouvido também deem suporte a 48 kHz. Observe que o recurso de ponto de extremidade de áudio virtual não está disponível no Windows 7 SP1.

O código de erro retornado pelo XAudio 2.9 quando ele não pode se recuperar automaticamente de uma alteração no ponto de extremidade de áudio é [XAUDIO2 \_ E \_ DEVICE \_ INVALIDATED](xaudio2-error-codes.md). No entanto, recomendamos que os aplicativos não codificam uma dependência no código de erro com um valor específico.

Para ser notificado sobre o erro, o aplicativo deve implementar a interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) e fornecer um ponteiro para essa interface invocando o método [**IXAudio2::RegisterForCallbacks.**](xaudio2-callbacks.md) A implementação do aplicativo [**de IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) será invocada pela API XAudio2 se ocorrer um erro durante a reprodução.

Observe que [**IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) não será necessariamente invocado se o pipeline de áudio estiver em pausa. Por exemplo, se o usuário minimizar o aplicativo ou o aplicativo for suspenso por qualquer motivo, a reprodução de áudio poderá ser pausada. Se a alteração no dispositivo de áudio ocorrer durante esse tempo, o erro só será retornado quando o aplicativo invocar [**IXAudio2::StartEngine**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-startengine) e/ou invocar [**IXAudio2SourceVoice::Start**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start). Se a reprodução puder ser pausada com seu aplicativo, você deverá testar a alteração do dispositivo de áudio enquanto a reprodução está em pausa, para verificar se o aplicativo ainda pode se recuperar dessa situação.

## <a name="xaudio-29-api-differences-compared-to-xaudio-27"></a>Diferenças de API do XAudio 2.9 em comparação com o XAudio 2.7

Esta seção fornece um resumo de algumas das diferenças de API entre o XAudio 2.7 e a versão redistribuível do XAudio 2.9.

### <a name="supported-formats"></a>Formatos com suporte

O XAudio 2.9 dá suporte a esses formatos de entrada no PC:

* PCM linear de 16 bits
* PCM Float linear de 32 bits
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
