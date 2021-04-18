---
title: Gravar playlists que contêm arquivos seguros
description: Gravar playlists que contêm arquivos seguros
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Media Format SDK, gravando listas de reprodução com arquivos seguros
- SDK do Windows Media Format, playlists com arquivos seguros
- ASF (Advanced Systems Format), gravando listas de reprodução com arquivos seguros
- ASF (formato de sistemas avançados), gravando listas de reprodução com arquivos seguros
- Formato de sistema avançado (ASF), listas de reprodução com arquivos seguros
- ASF (formato de sistemas avançados), listas de reprodução com arquivos seguros
- DRM (gerenciamento de direitos digitais), gravando listas de reprodução com arquivos seguros
- DRM (gerenciamento de direitos digitais), gravação de listas de reprodução com arquivos seguros
- DRM (gerenciamento de direitos digitais), listas de reprodução com arquivos seguros
- DRM (gerenciamento de direitos digitais), listas de reprodução com arquivos seguros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "105787679"
---
# <a name="burning-playlists-that-contain-secure-files"></a>Gravar playlists que contêm arquivos seguros

As licenças criadas usando os objetos do SDK do Windows Media Rights Manager 10 podem especificar o direito de copiar um arquivo para um CD como parte de uma lista de reprodução. Esse recurso, chamado de gravação de playlist, requer que você verifique as licenças de todos os arquivos na lista de reprodução antes de começar a copiar os dados. O Windows Media Format SDK fornece a interface [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) para executar a verificação de arquivos para você.

Para implementar a gravação da lista de reprodução, execute as seguintes etapas:

1.  Crie uma instância do objeto leitor ou o objeto leitor síncrono. Para obter mais informações, consulte [lendo arquivos ASF](reading-asf-files.md).
2.  Chame o método **QueryInterface** da interface do leitor ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) ou [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) para obter um ponteiro para a interface [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) .
3.  Copie os nomes de arquivo da lista de reprodução em uma matriz de cadeias de caracteres largos. Os nomes de arquivo na matriz devem estar na mesma ordem em que aparecem na lista de reprodução.
4.  Chame o método [**IWMReaderPlaylistBurn:: InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) , passando um ponteiro para a matriz criada na etapa 3, para inicializar a verificação de licença para os arquivos.
5.  Quando a verificação de licença é concluída, o objeto leitor envia uma \_ \_ mensagem de \_ gravação de WMT init para a implementação do método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Quando o retorno de chamada receber essa mensagem, chame o método [**IWMReaderPlaylistBurn:: GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) para obter os resultados da verificação de licença. Esse método usa uma matriz de variáveis **HRESULT** que correspondem aos nomes de arquivo na matriz passada para **InitPlaylistBurn**. Se todos os valores na matriz de resultados forem iguais a S \_ OK, você poderá continuar. Se qualquer resultado for um código de erro, a lista de reprodução não deverá ser copiada.
6.  Usando a mesma instância do leitor, abra e Leia cada arquivo. Você deve abrir os arquivos na ordem em que os nomes de arquivo exibidos na matriz de nome de arquivo passado para **InitPlaylistBurn**.
7.  Quando você copiou todos os arquivos na lista de reprodução, chame o [**IWMReaderPlaylistBurn:: EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) para concluir o processo de gravação da playlist e libere os recursos usados pelo leitor.

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




