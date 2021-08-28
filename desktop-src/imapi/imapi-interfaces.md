---
title: Interfaces IMAPi
description: As tabelas a seguir identificam e descrevem brevemente as interfaces usadas pelos desenvolvedores C/C++ e o objeto de script associado. Prefixe o nome do objeto na tabela com \ 0034; IMAPI2. \ 0034; para qualificar totalmente o nome do objeto ao criar o objeto no script.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c093acd587f975859d68fda23f6c1f169d969a78
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466165"
---
# <a name="imapi-interfaces"></a>Interfaces IMAPi

As tabelas a seguir identificam e descrevem brevemente as interfaces usadas pelos desenvolvedores C/C++ e o objeto de script associado. Prefixe o nome do objeto na tabela com "IMAPI2". para qualificar totalmente o nome do objeto ao criar o objeto no script.

A tabela a seguir lista as interfaces associadas aos dispositivos, ao mecanismo de gravação e ao formato gravadores e borracha.




| | | Interface | Objeto | | Mecanismo de gravação de nível baixo.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></li></ul> | MsftWriteEngine2 | | Gravador de imagem principal.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></li></ul> | MsftDiscFormat2Data | | Borracha de disco.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></li></ul> | MsftDiscFormat2Erase | | Gravador de imagem bruto.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></li></ul> | MsftDiscFormat2RawCD | | Gravador de imagem de acompanhamento.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></li></ul> | MsftDiscFormat2TrackAtOnce | | Enumeração de dispositivos de disco na lista de hardware do sistema.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></li></ul> | MsftDiscMaster2 | | Delegado de notificação para o objeto MsftDiscMaster2.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></li></ul> | DDiscMaster2Events | | Dispositivo de gravação individual.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></li></ul> | MsftDiscRecorder2 | | Atributos de gravação de dispositivo, incluindo o tipo de mídia, a velocidade de gravação e o tipo de controle de velocidade angular.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></li></ul> | MsftWriteSpeedDescriptor | 




 

A tabela a seguir lista as interfaces do sistema de arquivos.




| | | Interface | Objeto | | Fluxo de imagem de inicialização e propriedades para integrar a imagem inicializável na imagem do disco.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></li></ul> | Bootoptions | | Imagem e propriedades do sistema de arquivos. Esse objeto inclui todas as faixas e referências à imagem de inicialização e à imagem de resultado.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></li></ul> | CFileSystemImage | | Contêiner do fluxo de dados fornecido pelo objeto do sistema de arquivos.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></li></ul> | FileSystemImageResult | | Item de diretório na imagem do sistema de arquivos.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></li></ul> | FsiDirectoryItem | | Item de arquivo na imagem do sistema de arquivos.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></li></ul> | FsiFileItem | | Interface que contém as propriedades comuns aos itens de arquivo e diretório.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></li></ul> | FsiItem | | Criação de imagem de CD bruta.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></li></ul> | MsftRawCDImageCreator | | Objeto do auxiliar de objeto de fluxo para concatenar vários fluxos.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></li></ul> | MsftStreamConcatenate | | Fluxo intercalado para adicionar à imagem do disco.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></li></ul> | MsftStreamInterleave | | Fluxo gerado por pseudo-aleatório.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></li></ul> | MsftStreamPrgn001 | | O objeto de script <strong>MsftStreamZero</strong> não é implementado como uma interface. | <a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a> | 




 

A tabela a seguir lista as interfaces auxiliares.




| | | Interface | Objeto | | Coleção de intervalos de setor em uma imagem do sistema de arquivos.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></li></ul> | Nenhum objeto correspondente | | Suporte à verificação de gravação.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></li></ul> | Nenhum objeto correspondente | | Enumerador de FsiItems para aplicativos C/C++.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></li></ul> | EnumFsiItems | | Enumerador de ProgressItems para aplicativos C/C++.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></li></ul> | EnumProgressItems | | <ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></li></ul> | FsiFileItem2 | | suporte à verificação de imagem ISO.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></li></ul> | Nenhum objeto correspondente | | Suporte a várias sessões.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></li></ul> | Nenhum objeto correspondente | | Suporte sequencial de várias sessões.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></li></ul> | MsftMultisessionSequential | | Nome do arquivo e blocos associados na imagem do resultado.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></li></ul> | ProgressItem | | Lista de imagens de resultado, dividida por nome de arquivo e blocos associados.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></li></ul> | ProgressItems | 




 

 

 




