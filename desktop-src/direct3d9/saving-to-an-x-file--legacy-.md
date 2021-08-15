---
description: Use o procedimento a seguir em aplicativos herdáveis para salvar dados e modelos de arquivo .x em um arquivo .x.
ms.assetid: 5401b381-3599-465a-b41b-e63b7372fc0e
title: Salvando em um arquivo X (herdado) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03070b25c8839ddd17ab698a4f017822004d027d978b5c4ce589491f2e8fb8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797778"
---
# <a name="saving-to-an-x-file-legacy-direct3d-9"></a>Salvando em um arquivo X (herdado) (Direct3D 9)

Use o procedimento a seguir em aplicativos herdáveis para salvar dados e modelos de arquivo .x em um arquivo .x.

1.  Use a [**função DirectXFileCreate**](directxfilecreate.md) para criar um [**objeto IDirectXFile.**](idirectxfile.md)
2.  Use o [**método IDirectXFile::RegisterTemplates**](idirectxfile--registertemplates.md) para informar o sistema de arquivos DirectX sobre os modelos que você usará.
3.  Use o [**método IDirectXFile::CreateSaveObject**](idirectxfile--createsaveobject.md) para criar [**um objeto IDirectXFileSaveObject.**](idirectxfilesaveobject.md)
4.  Use o [**método IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md) para salvar modelos, se desejado.
5.  Loop pelos objetos a salvar. Para cada objeto de nível superior, execute as etapas a seguir.
    -   Use o [**método IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para criar um objeto [**IDirectXFileData**](idirectxfiledata.md) como um objeto de nível superior no arquivo. Se o objeto de dados de nível superior tiver objetos filho opcionais, adicione-os ao objeto usando o método apropriado da próxima etapa.
    -   Cada [**objeto IDirectXFileData**](idirectxfiledata.md) poderá ter objetos filho opcionais se seu modelo permitir. Os objetos filho podem ser qualquer um dos três tipos de objetos: **IDirectXFileData,** [**IDirectXFileDataReference**](idirectxfiledatareference.md)ou [**IDirectXFileBinary.**](idirectxfilebinary.md) Loop pelos objetos que você precisa salvar, adicionando cada membro filho opcional à lista de objetos da maneira apropriada para seu tipo, conforme ilustrado nas etapas a seguir. Em seguida, se o tipo de objeto for Dados, chame o método [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para criar um **objeto IDirectXFileData** e, em seguida, chame o método [**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md) para adicioná-lo como um filho do objeto. Se o tipo de objeto for Referência de Dados, chame o método [**IDirectXFileData::AddDataReference**](idirectxfiledata--adddatareference.md) para criar e adicionar o objeto de referência de dados como um filho do objeto . Ou, se o tipo de objeto for Binary, chame o método [**IDirectXFileData::AddBinaryObject**](idirectxfiledata--addbinaryobject.md) para criar e adicionar o objeto binário como um filho do objeto .
    -   Chame o [**método IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) para salvar o objeto de dados e seus filhos.
    -   Libere o [**objeto IDirectXFileData.**](idirectxfiledata.md)
6.  Libere o [**objeto IDirectXFileSaveObject.**](idirectxfilesaveobject.md)
7.  Libere o [**objeto IDirectXFile.**](idirectxfile.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquivos X (herdados)](x-files--legacy-.md)
</dt> </dl>

 

 



