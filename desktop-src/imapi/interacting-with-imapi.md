---
title: Interagindo com IMAPi
description: As etapas a seguir descrevem uma interação típica entre um aplicativo e o IMAPi.
ms.assetid: e57a86c4-7e27-40cf-a9c1-081b3f20d9d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab97d1a9d76d1e82dab64fb777ef5207d3d47560b2a889981c698ab78e3622b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726986"
---
# <a name="interacting-with-imapi"></a>Interagindo com IMAPi

As etapas a seguir descrevem uma interação típica entre um aplicativo e o IMAPi.

1.  Crie uma instância do **MSDiscMasterObj** (usando **CoCreateInstance**, apontadores inteligentes de uma importação e assim por diante) e solicite a interface [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) .
2.  Adquira acesso ao IMAPi chamando [**IDiscMaster:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open). Se essa chamada for bem sucedido, o aplicativo terá acesso completo a todas as interfaces e métodos implementados no **MSDiscMasterObj**.
3.  Recupere o enumerador de formato mestre de disco usando [**EnumDiscMasterFormats**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscmasterformats). Enumere o conjunto de formatos que o objeto mestre de disco dá suporte e, em seguida, selecione o formato ativo. Os formatos retornados do enumerador são o IIDs das interfaces para [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) e [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster).
4.  Recupere o enumerador do gravador de disco usando [**EnumDiscRecorders**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscrecorders). Enumere a lista de gravadores de disco com suporte (específicos ao formato ativo) e, em seguida, selecione o gravador ativo. A interface [**IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) representa um dispositivo físico.
5.  Use [**IDiscMaster::P rogressadvise**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-progressadvise) para se registrar para retornos de chamada de andamento.
6.  Use a interface para o formato selecionado para criar conteúdo. O conteúdo é compilado de forma incremental, de modo que o conteúdo das trilhas ou da pasta pode ser adicionado a uma parte do disco. A criação desse conteúdo é chamada *de preparo de uma imagem*. O conteúdo da imagem preparada não pode ser excluído incrementalmente (não é possível remover uma faixa que foi adicionada), mas é possível limpar o conteúdo de uma imagem preparada para que o preparo possa ser iniciado novamente. Use [**IDiscMaster:: ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) para reiniciar o preparo.

* * Para áudio: * *

1.  Use [**IRedbookDiscMaster:: CreateAudioTrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-createaudiotrack) para indicar que uma nova faixa de áudio está sendo iniciada no disco.
2.  Use [**IRedbookDiscMaster:: AddAudioTrackBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks) para adicionar dados brutos de áudio a um controle. O aplicativo pode usar [**GetAvailableAudioTrackBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getavailableaudiotrackblocks), [**GetTotalAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-gettotalaudioblocks)e [**GetUsedAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getusedaudioblocks) para recuperar informações estatísticas.
3.  Use [**IRedbookDiscMaster:: CloseAudioTrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-closeaudiotrack) para fechar uma faixa de áudio.
4.  Repita as etapas de 1-3 até sem espaço ou todas as faixas de áudio foram gravadas.

* * Para dados: * *

1.  Use [**IJolietDiscMaster:: AddData**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-adddata) para adicionar o conteúdo de uma pasta à imagem. Os itens dentro de uma pasta são colocados na raiz do arquivo de imagem. Use [**GetTotalDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-gettotaldatablocks) e [**GetUsedDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-getuseddatablocks) para recuperar informações estatísticas.
2.  Repita a etapa acima até sem espaço ou todos os dados tiverem sido adicionados.

* * Para todos os discos: * *

1.  Use [**IDiscMaster:: RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) para registrar o disco.
2.  Feche a sessão IMAPi usando [**IDiscMaster:: Close**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-close). Fechar a sessão limpa o conteúdo do disco stash.

 

 




