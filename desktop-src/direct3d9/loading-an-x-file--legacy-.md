---
description: Use o procedimento a seguir em aplicativos herdados para carregar um arquivo. x.
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: Carregando um arquivo X (Herdado) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8ac27c43ba33f6bd0408403d6390d4855f2644182d82f1ad8e84e5939f98ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846516"
---
# <a name="loading-an-x-file-legacy-direct3d-9"></a>Carregando um arquivo X (Herdado) (Direct3D 9)

Use o procedimento a seguir em aplicativos herdados para carregar um arquivo. x.

1.  Use a função [**DirectXFileCreate**](directxfilecreate.md) para criar um objeto [**IDirectXFile**](idirectxfile.md) .
2.  Se os modelos estiverem presentes no arquivo DirectX que você carregará, use o método [**IDirectXFile:: RegisterTemplates**](idirectxfile--registertemplates.md) para registrar esses modelos.
3.  Use o método [**IDirectXFile:: Createenumobject**](idirectxfile--createenumobject.md) para criar um objeto enumerador [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .
4.  Faça um loop pelos objetos no arquivo. Para cada objeto, execute as etapas a seguir.
    1.  Use o método [**IDirectXFileEnumObject:: GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) para recuperar cada objeto [**IDirectXFileData**](idirectxfiledata.md) .
    2.  Use o método [**IDirectXFileData:: GetType**](idirectxfiledata--gettype.md) para recuperar o tipo de dados.
    3.  Carregue os dados usando o método [**IDirectXFileData:: GetData**](idirectxfiledata--getdata.md) .
    4.  Se o objeto tiver membros opcionais, recupere os membros opcionais chamando o método [**IDirectXFileData:: GetNextObject**](idirectxfiledata--getnextobject.md) .
    5.  Libere o objeto [**IDirectXFileData**](idirectxfiledata.md) .
5.  Libere o objeto [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .
6.  Libere o objeto [**IDirectXFile**](idirectxfile.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquivos X (herdados)](x-files--legacy-.md)
</dt> </dl>

 

 



