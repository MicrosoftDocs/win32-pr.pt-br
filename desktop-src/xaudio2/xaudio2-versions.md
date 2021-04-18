---
description: O XAudio2 é uma API de plataforma cruzada que foi enviada para uso no Xbox 360, bem como em versões do Windows, incluindo o Windows XP, o Windows Vista, o Windows 7 e o Windows 8.
ms.assetid: 875b44c4-30d6-8a6e-0cfc-9beb8c46f1b4
title: Versões do XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c9facfe357c323bd8f7b607460a8f59bd062fe
ms.sourcegitcommit: 010f524cd6098a5941de77907d4d6ae7871f8af1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "105813088"
---
# <a name="xaudio2-versions"></a>Versões do XAudio2

O XAudio2 é uma API de plataforma cruzada que foi enviada para uso no Xbox 360, bem como em versões do Windows, incluindo o Windows XP, o Windows Vista, o Windows 7 e o Windows 8. No Xbox 360, o XAudio2 é fornecido como uma biblioteca estática que é compilada no executável do jogo principal. No Windows, o XAudio2 é fornecido como uma DLL (biblioteca de vínculo dinâmico) instalada nas pastas do sistema do sistema operacional.

## <a name="xaudio-29-windows-10-and-redistributable-for-windows-7-and-windows-8x"></a>XAudio 2,9 (Windows 10 e redistribuível para Windows 7 e Windows 8. x)

A versão 2,9 do XAudio2 é fornecida como parte do Windows 10, XAUDIO2 \_9.DLL, juntamente com XAudio 2,8 para dar suporte a aplicativos mais antigos. Uma [versão redistribuível do XAudio 2,9](xaudio2-redistributable.md) também está disponível para Windows 7 SP1, Windows 8 e Windows 8.1.

O XAudio 2.9 foi atualizado com as seguintes alterações:

-   Novos sinalizadores de criação: \_ \_ mecanismo de depuração XAUDIO2, XAudio2 \_ parar \_ mecanismo \_ quando \_ ocioso, XAudio2 \_ 1024 \_ Quantum
-   o suporte a xWMA está disponível nesta versão do XAudio2.
-   A função [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) tem suporte na versão do Windows 10 do XAudio 2,9.
-   [**XAUDIO2FX \_ Os \_ parâmetros de reverberação**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) agora incluem o valor *SideDelay* para sistemas 7,1.
-   A função [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative) agora inclui o parâmetro *sevenDotOneReverb* booliano habilitando o reverbo 7,1.

## <a name="xaudio-28-windows-8x"></a>XAudio 2,8 (Windows 8. x)

A versão 2,8 do XAudio2 é fornecida hoje como um componente do sistema no Windows 8, XAUDIO2 \_8.DLL. Ele está disponível "Inbox" e não requer redistribuição com um aplicativo. É recomendável usar o SDK (Software Development Kit) do Windows para Windows 8 para desenvolver em relação ao XAudio2; o SDK do Windows para o Windows 8 contém o cabeçalho e a biblioteca de importação necessários para vinculação estática com o XAUDIO2 \_8.DLL.

O XAudio2 2,8 foi atualizado com as seguintes alterações:

-   Esta versão dá suporte ao desenvolvimento de aplicativos da Windows Store; a API XAudio2 pode ser usada em aplicativos C++/DirectX da Windows Store.
-   [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) é uma chamada de API do Win32 simples e não cria mais um CLSID XAudio2. O suporte para instanciar XAudio2 por CoCreateInstance foi removido.
-   A função Initialize agora é chamada implicitamente pelo processo de criação e foi removida da interface [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .
-   A funcionalidade de enumeração de dispositivo foi removida do XAudio2; as funções GetDeviceDetails e GetDeviceCount foram removidas da interface [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) . Os aplicativos que desejam renderizar para outros dispositivos de áudio no sistema devem passar uma cadeia de caracteres de identificador de dispositivo para [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) em vez de um índice de dispositivo. O dispositivo de processamento de áudio padrão ainda pode ser criado sem enumeração.
-   [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) tem uma função adicionada [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) para que retorna a máscara de canal para o dispositivo de saída de destino.
-   As bibliotecas [X3DAudio](x3daudio.md) e [xapofx](xapofx-overview.md) são mescladas em XAudio2. O código do aplicativo ainda usa cabeçalhos separados, X3DAUDIO. H e XPOFX. H, mas agora é vinculado a uma única biblioteca de importação, XAUDIO2 \_ 8. lib.
-   o suporte a xWMA não está disponível nesta versão do XAudio2; xWMA não terá suporte como um formato de buffer de áudio ao chamar CreateSourceVoice. Agora, recomendamos o objeto leitor de fonte Media Foundation para decodificar uma ampla variedade de formatos de mídia em buffers PCM na memória.
-   [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) agora usa quatro parâmetros em vez de dois. Os parâmetros mais recentes especificam dados iniciais como parte da criação do [xapofx](xapofx-overview.md) .

## <a name="xaudio-27-and-earlier-windows-7"></a>XAudio 2,7 e anterior (Windows 7)

Todas as versões anteriores do XAudio2 para uso em aplicativos foram fornecidas como DLLs redistribuíveis no SDK do DirectX. A primeira versão do XAudio2, XAudio2 2,0, foi fornecida na versão de 2008 de março do SDK do DirectX. A última versão a ser enviada no SDK do DirectX foi a XAudio2 2,7, disponível na última versão do SDK do DirectX em junho de 2010.

O SDK do DirectX herdado não está mais disponível nos downloads da Microsoft devido à desativação de todo o conteúdo do SHA-1 assinado. Junho de 2010 foi a versão final da vida útil.

As versões anteriores do XAudio2 não podem ser usadas para criar aplicativos da Windows Store para Windows 8.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> <dt>

[Principais conceitos do XAudio2](xaudio2-key-concepts.md)
</dt> </dl>

[Guia do desenvolvedor para a versão redistribuível do XAudio 2.9](xaudio2-redistributable.md)
</dt> </dl>
 

 
