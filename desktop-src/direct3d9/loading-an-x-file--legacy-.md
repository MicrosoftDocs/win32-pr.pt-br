---
description: Use o procedimento a seguir em aplicativos herdados para carregar um arquivo. x.
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: Carregando um arquivo X (Herdado) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ed54afdc7d1aa18fdde992a0799a8990a49c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500329"
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

 

 



