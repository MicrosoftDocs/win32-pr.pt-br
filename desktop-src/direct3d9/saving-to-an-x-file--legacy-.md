---
description: Use o procedimento a seguir em aplicativos herdados para salvar dados e modelos de arquivo. x em um arquivo. x.
ms.assetid: 5401b381-3599-465a-b41b-e63b7372fc0e
title: Salvando em um arquivo X (Herdado) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467f824c8e3ab9cd360a93d3f69fd1a2352548ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104295988"
---
# <a name="saving-to-an-x-file-legacy-direct3d-9"></a>Salvando em um arquivo X (Herdado) (Direct3D 9)

Use o procedimento a seguir em aplicativos herdados para salvar dados e modelos de arquivo. x em um arquivo. x.

1.  Use a função [**DirectXFileCreate**](directxfilecreate.md) para criar um objeto [**IDirectXFile**](idirectxfile.md) .
2.  Use o método [**IDirectXFile:: RegisterTemplates**](idirectxfile--registertemplates.md) para informar ao sistema de arquivos do DirectX sobre todos os modelos que serão usados.
3.  Use o método [**IDirectXFile:: Createsaveobject**](idirectxfile--createsaveobject.md) para criar um objeto [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) .
4.  Use o método [**IDirectXFileSaveObject:: SaveTemplates**](idirectxfilesaveobject--savetemplates.md) para salvar modelos, se desejado.
5.  Faça um loop pelos objetos para salvar. Para cada objeto de nível superior, execute as etapas a seguir.
    -   Use o método [**IDirectXFileSaveObject:: Createdataobject**](idirectxfilesaveobject--createdataobject.md) para criar um objeto [**IDirectXFileData**](idirectxfiledata.md) como um objeto de nível superior no arquivo. Se o objeto de dados de nível superior tiver objetos filho opcionais, adicione-os ao objeto usando o método apropriado da próxima etapa.
    -   Cada objeto [**IDirectXFileData**](idirectxfiledata.md) pode ter objetos filho opcionais se o seu modelo permitir. Os objetos filho podem ser qualquer um dos três tipos de objetos: **IDirectXFileData**, [**IDirectXFileDataReference**](idirectxfiledatareference.md)ou [**IDirectXFileBinary**](idirectxfilebinary.md). Faça um loop pelos objetos que você precisa salvar, adicionando cada membro filho opcional à lista de objetos da maneira apropriada ao seu tipo, conforme ilustrado nas etapas a seguir. Em seguida, se o tipo de objeto for dado, chame o método [**IDirectXFileSaveObject:: Createdataobject**](idirectxfilesaveobject--createdataobject.md) para criar um objeto **IDirectXFileData** e, em seguida, chame o método [**IDirectXFileData:: adddataobject**](idirectxfiledata--adddataobject.md) para adicioná-lo como um filho do objeto. Se o tipo de objeto for referência de dados, chame o método [**IDirectXFileData:: AddDataReference**](idirectxfiledata--adddatareference.md) para criar e adicionar o objeto de referência de dados como um filho do objeto. Ou, se o tipo de objeto for Binary, chame o método [**IDirectXFileData:: Addbinaryobject**](idirectxfiledata--addbinaryobject.md) para criar e adicionar o objeto Binary como um filho do objeto.
    -   Chame o método [**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md) para salvar o objeto de dados e seus filhos.
    -   Libere o objeto [**IDirectXFileData**](idirectxfiledata.md) .
6.  Libere o objeto [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) .
7.  Libere o objeto [**IDirectXFile**](idirectxfile.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquivos X (herdados)](x-files--legacy-.md)
</dt> </dl>

 

 



