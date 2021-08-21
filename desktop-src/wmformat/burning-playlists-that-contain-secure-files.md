---
title: Gravar playlists que contêm arquivos seguros
description: Gravar playlists que contêm arquivos seguros
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows SDK de Formato de Mídia, playlists de gravação com arquivos seguros
- Windows SDK de Formato de Mídia, playlists com arquivos seguros
- ASF (Advanced Systems Format), playlists de gravação com arquivos seguros
- ASF (Formato de Sistemas Avançados), playlists de gravação com arquivos seguros
- ASF (Advanced Systems Format), playlists com arquivos seguros
- ASF (Formato de Sistemas Avançados), playlists com arquivos seguros
- DRM (gerenciamento de direitos digitais), playlists de gravação com arquivos seguros
- DRM (gerenciamento de direitos digitais), playlists de gravação com arquivos seguros
- DRM (gerenciamento de direitos digitais), listas de reprodução com arquivos seguros
- DRM (gerenciamento de direitos digitais), playlists com arquivos seguros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d43cfbf3bb6e8ce4bac5cc1006fe73292988547ef2fc35289a4ced13e6f0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028114"
---
# <a name="burning-playlists-that-contain-secure-files"></a>Gravar playlists que contêm arquivos seguros

As licenças criadas usando os objetos do SDK do Windows Media Rights Manager 10 podem especificar o direito de copiar um arquivo para compact disc como parte de uma playlist. Esse recurso, chamado gravação de playlist, requer que você verifique as licenças de todos os arquivos na playlist antes de começar a copiar dados. O Windows SDK de Formato de Mídia fornece a interface [**IWMReaderPlaylistPlay Para**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) executar a verificação de arquivo para você.

Para implementar a gravação da playlist, execute as seguintes etapas:

1.  Crie uma instância do objeto de leitor ou o objeto de leitor síncrono. Para obter mais informações, consulte [Lendo arquivos ASF](reading-asf-files.md).
2.  Chame o método **QueryInterface** da interface de leitor ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) ou [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) para obter um ponteiro para a interface [**IWMReaderPlaylistFace.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn)
3.  Copie os nomes de arquivo da playlist em uma matriz de cadeias de caracteres largos. Os nomes de arquivo na matriz devem estar na mesma ordem que aparecem na playlist.
4.  Chame o método [**IWMReaderPlaylistPlay::InitPlaylist Widget,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) passando um ponteiro para a matriz criada na etapa 3, para inicializar a verificação de licença para os arquivos.
5.  Quando a verificação de licença é concluída, o objeto leitor envia uma mensagem WMT INIT PLAYLIST BURN para sua implementação do método de retorno de chamada \_ \_ \_ [**IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Quando o retorno de chamada receber essa mensagem, chame o método [**IWMReaderPlaylistRead::GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) para obter os resultados da verificação de licença. Esse método aceita uma matriz de **variáveis HRESULT** que correspondem aos nomes de arquivo na matriz passada para **InitPlaylist Ltda.** Se todos os valores na matriz de resultados são iguais a S \_ OK, você pode continuar. Se qualquer resultado for um código de erro, a playlist não deverá ser copiada.
6.  Usando a mesma instância do leitor, abra e leia cada arquivo. Você deve abrir os arquivos na ordem em que os nomes de arquivo aparecem na matriz de nomes de arquivo passada para **InitPlaylist Ltda.**
7.  Depois de copiar todos os arquivos na playlist, chame [**O IWMReaderPlaylistPlaylistPlay::EndPlaylist Ltda**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) para concluir o processo de gravar playlist e liberar os recursos usados pelo leitor.

> [!Note]  
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




