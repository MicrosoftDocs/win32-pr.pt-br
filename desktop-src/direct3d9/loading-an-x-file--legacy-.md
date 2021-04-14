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
# <a name="loading-an-x-file-legacy-direct3d-9"></a><span data-ttu-id="62f65-103">Carregando um arquivo X (Herdado) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="62f65-103">Loading an X File (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="62f65-104">Use o procedimento a seguir em aplicativos herdados para carregar um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="62f65-104">Use the following procedure in legacy applications to load a .x file.</span></span>

1.  <span data-ttu-id="62f65-105">Use a função [**DirectXFileCreate**](directxfilecreate.md) para criar um objeto [**IDirectXFile**](idirectxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="62f65-105">Use the [**DirectXFileCreate**](directxfilecreate.md) function to create an [**IDirectXFile**](idirectxfile.md) object.</span></span>
2.  <span data-ttu-id="62f65-106">Se os modelos estiverem presentes no arquivo DirectX que você carregará, use o método [**IDirectXFile:: RegisterTemplates**](idirectxfile--registertemplates.md) para registrar esses modelos.</span><span class="sxs-lookup"><span data-stu-id="62f65-106">If templates are present in the DirectX file that you will load, use the [**IDirectXFile::RegisterTemplates**](idirectxfile--registertemplates.md) method to register those templates.</span></span>
3.  <span data-ttu-id="62f65-107">Use o método [**IDirectXFile:: Createenumobject**](idirectxfile--createenumobject.md) para criar um objeto enumerador [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="62f65-107">Use the [**IDirectXFile::CreateEnumObject**](idirectxfile--createenumobject.md) method to create an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) enumerator object.</span></span>
4.  <span data-ttu-id="62f65-108">Faça um loop pelos objetos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="62f65-108">Loop through the objects in the file.</span></span> <span data-ttu-id="62f65-109">Para cada objeto, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="62f65-109">For each object, perform the following steps.</span></span>
    1.  <span data-ttu-id="62f65-110">Use o método [**IDirectXFileEnumObject:: GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) para recuperar cada objeto [**IDirectXFileData**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="62f65-110">Use the [**IDirectXFileEnumObject::GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) method to retrieve each [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
    2.  <span data-ttu-id="62f65-111">Use o método [**IDirectXFileData:: GetType**](idirectxfiledata--gettype.md) para recuperar o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="62f65-111">Use the [**IDirectXFileData::GetType**](idirectxfiledata--gettype.md) method to retrieve the data's type.</span></span>
    3.  <span data-ttu-id="62f65-112">Carregue os dados usando o método [**IDirectXFileData:: GetData**](idirectxfiledata--getdata.md) .</span><span class="sxs-lookup"><span data-stu-id="62f65-112">Load the data using the [**IDirectXFileData::GetData**](idirectxfiledata--getdata.md) method.</span></span>
    4.  <span data-ttu-id="62f65-113">Se o objeto tiver membros opcionais, recupere os membros opcionais chamando o método [**IDirectXFileData:: GetNextObject**](idirectxfiledata--getnextobject.md) .</span><span class="sxs-lookup"><span data-stu-id="62f65-113">If the object has optional members, retrieve the optional members by calling the [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) method.</span></span>
    5.  <span data-ttu-id="62f65-114">Libere o objeto [**IDirectXFileData**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="62f65-114">Release the [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
5.  <span data-ttu-id="62f65-115">Libere o objeto [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="62f65-115">Release the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) object.</span></span>
6.  <span data-ttu-id="62f65-116">Libere o objeto [**IDirectXFile**](idirectxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="62f65-116">Release the [**IDirectXFile**](idirectxfile.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62f65-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62f65-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62f65-118">Arquivos X (herdados)</span><span class="sxs-lookup"><span data-stu-id="62f65-118">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



