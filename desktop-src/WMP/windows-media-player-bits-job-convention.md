---
title: Windows Media Player Convenção de trabalho BITS
description: Windows Media Player pode baixar e adicionar automaticamente itens de mídia digital à biblioteca se você usar Serviço de Transferência Inteligente em Segundo Plano (BITS).
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- Windows Media Player lojas online, Serviço de Transferência Inteligente em Segundo Plano (BITS)
- lojas online, Serviço de Transferência Inteligente em Segundo Plano (BITS)
- tipo 2 lojas online, Serviço de Transferência Inteligente em Segundo Plano (BITS)
- Serviço básico de transferência inteligente (BITS)
- BITS (Serviço de Transferência Inteligente em Segundo Plano)
- Windows Media Player lojas online, convenção de trabalho BITS
- lojas online, Convenção de trabalho BITS
- tipo 2 lojas online, Convenção de trabalho BITS
- Convenção de trabalho BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa62b3d5691abe6f91afde1cda4d83525159d2708cfde80d0ae3f23259003e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117931227"
---
# <a name="windows-media-player-bits-job-convention"></a>Windows Media Player Convenção de trabalho BITS

Windows Media Player pode baixar e adicionar automaticamente itens de mídia digital à biblioteca se você usar [Serviço de Transferência Inteligente em Segundo Plano (BITS)](/windows/desktop/Bits/background-intelligent-transfer-service-portal). Para aproveitar esse recurso, você deve adicionar seu trabalho à fila de transferência de BITS e chamar **método ibackgroundcopyjob:: SetDescription**, fornecendo uma cadeia de caracteres de descrição que usa o formato correto.

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

## <a name="syntax"></a>Sintaxe

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*
</dt> <dd>

um valor de 32 bits gerado aleatoriamente que Windows Media Player usa para identificar o serviço.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Operador*
</dt> <dd>

O nome do provedor. Esse valor deve corresponder a um nome de chave de loja online válido.

</dd> <dt>

<span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*
</dt> <dd>

O nome do artista principal para o álbum.

</dd> <dt>

<span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*Campos AlbumTitle*
</dt> <dd>

O título do álbum.

</dd> <dt>

<span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*
</dt> <dd>

O número de faixas do CD.

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Título*
</dt> <dd>

O título do conteúdo.

</dd> <dt>

<span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Permanência*
</dt> <dd>

A duração do conteúdo.

</dd> <dt>

<span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Avaliações*
</dt> <dd>

A classificação do conteúdo.

</dd> </dl>

## <a name="remarks"></a>Comentários

quando o Windows Media Player 10 ou posterior usa BITS para baixar conteúdo, ele enumera os trabalhos na fila de transferência e inspeciona a cadeia de caracteres de descrição para cada trabalho. se a cadeia de caracteres de descrição corresponder à convenção esperada, Windows Media Player baixará o conteúdo.

Você deve adicionar apenas um arquivo de mídia digital para download em cada trabalho do BITS.

depois de iniciar um trabalho do BITS usando essa convenção, você deve permitir que Windows Media Player conclua o trabalho. Windows Media Player também removerá o trabalho da fila BITS, moverá o arquivo baixado para o local em que a música copiada é salva e adicionará o arquivo baixado à biblioteca.

O parâmetro *ServiceId* deve conter um valor de 32 bits diferente de zero. Recomendamos que você use a função [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para criar esse valor.

O nome de arquivo que você especifica usando o parâmetro *LocalName* de **método ibackgroundcopyjob:: AddFile** deve ter uma extensão de nome de arquivo. WMA,. wmv, .mp3 ou. ASF.

Os parâmetros restantes são projetados para conter valores de metadados relacionados ao conteúdo. Você pode recuperar esses valores da página da Web da loja online usando **DownloadItem. getItemInfo**. Você pode recuperar a coleção de download correta chamando **DownloadManager. Getbaixecollection** e fornecendo *ServiceId* como o parâmetro *CollectionId* .

Windows Media Player inspeciona a fila BITS periodicamente enquanto o Player está em execução. para garantir que Windows Media Player verifique a fila BITS para trabalhos de download, você deve criar um valor na seguinte subchave do registro:

**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ Services**

O valor deve ser criado da seguinte maneira.



| Nome                | Tipo      | Descrição                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RefreshDownload** | **DWORD** | especifica se Windows Media Player deve inspecionar a fila BITS para trabalhos de download. Se o valor for zero, o Player não inspecionará a fila do BITS. O Player deve inspecionar a fila se o valor for diferente de zero. |



 

você pode usar a seguinte sintaxe alternativa para adicionar trabalhos do BITS que Windows Media Player não é concluído, mas para o qual ele simplesmente mostra informações de status:

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

Ao usar a sintaxe anterior, você deve escrever o código para concluir o download do BITS, organizar o conteúdo no computador do usuário e adicionar o conteúdo à biblioteca, se desejado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[CryptGenRandom](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[**DownloadItem.getItemInfo**](downloaditem-getiteminfo.md)
</dt> <dt>

[**DownloadManager. getbaixecollection**](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[**Referência para lojas online do tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 